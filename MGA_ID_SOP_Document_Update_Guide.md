# ADO 1036196 -- MGA ID Update for SOP Documents

## 1. Current code issue

In `DataService2Bean.java`, the code around lines 828--834 still
references `mGAIdVerification` through `setMGAIdVerification(...)`.

The field declaration:

``` java
private transient MGAIdVerification mGAIdVerification;
```

has already been removed. Therefore, the setter reference produces a
compile error such as:

``` text
mGAIdVerification cannot be resolved
```

Under the proposed design, remove all three of the following from
`DataService2Bean.java`:

-   `private transient MGAIdVerification mGAIdVerification;`
-   `setMGAIdVerification(...)`
-   `getMGAIdVerification(...)`

Also remove the old `checkAndUpdateMgaId(...)` implementation if it is
no longer part of the interface or call flow.

The new design keeps the business decision in `Part1FormValidation` and
performs the document database update directly in `DataService2Bean`. A
separate Spring bean lookup through `getBeanFromApplicationContext(...)`
is therefore not required for this flow.

> **Important:** Confirm that no other class still references
> `MGAIdVerification` or the removed methods before deleting the class
> or its remaining references.

------------------------------------------------------------------------

## 2. End-to-end call hierarchy and data flow

``` text
Part1FormValidation.java
(CaseProcessingEJB)
    |
    |-- 1. part1ODVO = dsBean2.getPart1OperationalData(caseId)
    |       |
    |       `-- GetPart1ODVO.java (DataServicesEJB)
    |               |
    |               `-- Reads DOCMT_INSTNC for EVDNCE_TY_PART1
    |                   using Docmt_instncFactory
    |                       |
    |                       `-- Sets part1ODVO.setMgaIDCd(
    |                               docmtInstncData.getMgaid_txt())
    |
    `-- 2. checkAndUpdateMGAIDCD(
            part1FDVO, part1ODVO, dsBean2, caseId, userName)
            |
            |-- Reads current MGA ID from part1ODVO.getMgaIDCd()
            |       `-- Avoids a duplicate database query
            |
            |-- If current MGA ID is not "GENPACT", return
            |
            |-- Reads signature description from:
            |       part1FDVO.getPart1RepresentationsFDVO()
            |           .getProposedInsuredSignatureStatus()
            |
            |-- Converts description to code using:
            |       VOUtilsCdForDescriptionForAV
            |           .getSignStsCdForDesc(...)
            |
            |-- Branch A: Not e-signed
            |       `-- targetMgaId = "NBS"
            |
            |-- Branch B: E-signed
            |       |
            |       |-- Reads BGA number from:
            |       |       part1FDVO.getPart1ManagingAgencyReportFDVO()
            |       |           .getAgencyNumber()
            |       |
            |       |-- Looks up configured MGA ID:
            |       |       dsBean2.getMgaIdByBgaAndSignType(
            |       |           bgaNumber, String.valueOf(signStatusCd))
            |       |
            |       |       `-- DataService2AccessBean
            |       |               `-- DataService2Bean
            |       |                       `-- MGAID_BGA_TY table
            |       |
            |       `-- If lookup result is null/blank:
            |               `-- targetMgaId = "EPB"
            |
            `-- Persists the update and synchronizes the in-memory value:
                    |
                    |-- dsBean2.updateMgaIdForSopDocuments(
                    |       caseId, targetMgaId)
                    |       |
                    |       `-- DataService2AccessBean
                    |               `-- DataService2Bean
                    |                       (@TransactionAttribute(REQUIRES_NEW))
                    |                           |
                    |                           `-- Docmt_instncFactory
                    |                               .findByCasenbr(caseId)
                    |                                   |
                    |                                   `-- Loops through documents,
                    |                                       filters the 7 SOP types,
                    |                                       and updates MGAID_TXT
                    |                                       in Oracle
                    |
                    `-- part1ODVO.setMgaIDCd(targetMgaId)
                            `-- Keeps the in-memory ODVO current for
                                the remaining validation logic
```

### Data sources used in this flow

  -------------------------------------------------------------------------------------------------------------------
  Data                                Source
  ----------------------------------- -------------------------------------------------------------------------------
  Current MGA ID                      `part1ODVO.getMgaIDCd()`

  Signature description               `part1FDVO.getPart1RepresentationsFDVO().getProposedInsuredSignatureStatus()`

  Signature status code               `VOUtilsCdForDescriptionForAV.getSignStsCdForDesc(...)`

  BGA number                          `part1FDVO.getPart1ManagingAgencyReportFDVO().getAgencyNumber()`

  Configured MGA ID                   `MGAID_BGA_TY`, accessed through `DataService2`

  SOP document records                `DOCMT_INSTNC`, accessed through `Docmt_instncFactory`
  -------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 3. Why each design change was made

  ----------------------------------------------------------------------------------------------------------------
  Change                                                           Reason                  Related concept
  ---------------------------------------------------------------- ----------------------- -----------------------
  Remove `MGAIdVerification` and the Spring                        The required data and   **Spring IoC /
  `getBeanFromApplicationContext(...)` lookup                      logic are available     ApplicationContext:**
                                                                   through the existing    Spring's application
                                                                   GENIUS flow.            context manages Spring
                                                                   `GetPart1ODVO` already  beans. A separate
                                                                   retrieves the current   lookup is unnecessary
                                                                   MGA ID, and the         when this
                                                                   database update can be  implementation no
                                                                   handled in              longer depends on that
                                                                   `DataService2Bean`.     helper bean.

  Place the MGA ID retrieval block at the end of                   This makes the final    **Value Object
  `GetPart1ODVO.java`, immediately before `return part1ODVO;`      ODVO contain the MGA ID pattern:** The FDVO
                                                                   retrieved from the      carries form data; the
                                                                   document record and     ODVO carries
                                                                   reduces the chance that operational data.
                                                                   later code overwrites   Reusing the ODVO avoids
                                                                   it.                     an additional database
                                                                                           read.

  Use `VOUtilsCdForDescriptionForAV` for signature conversion      GENIUS already provides **DRY / shared
                                                                   a centralized           utility:** Reusing
                                                                   conversion from the     existing conversion
                                                                   signature description   logic avoids
                                                                   shown in the UI to its  duplicating mappings
                                                                   corresponding database  and string comparisons.
                                                                   code.                   

  Keep the `DataService2` → `DataService2AccessBean` →             `Part1FormValidation`   **EJB facade /
  `DataService2Bean` call path                                     and the document entity AccessBean pattern:**
                                                                   implementation belong   The interface exposes
                                                                   to different EJB        the operation, the
                                                                   modules. The service    AccessBean handles EJB
                                                                   facade provides the     lookup, and the bean
                                                                   cross-module access     implements the service.
                                                                   point.                  

  Use                                                              The intended behavior   **Container-Managed
  `@TransactionAttribute(TransactionAttributeType.REQUIRES_NEW)`   is to run the document  Transactions:** The EJB
  on the update method                                             update in a separate    container suspends the
                                                                   transaction from the    caller transaction,
                                                                   caller's transaction.   runs the method in a
                                                                                           new transaction, and
                                                                                           then resumes the caller
                                                                                           transaction.

  Use `PortableRemoteObject.narrow(...)` and                       The factory returns     **EJB 2.x remote entity
  `setDocmt_instncData(...)`                                       remote EJB references.  beans:** `narrow(...)`
                                                                   The code narrows the    converts a remote
                                                                   returned reference,     reference to the
                                                                   obtains the data        expected remote
                                                                   object, changes it, and interface. Updating the
                                                                   passes the updated data detached data object
                                                                   object back to the      alone may not persist
                                                                   entity bean.            it; the entity bean
                                                                                           setter is used to apply
                                                                                           the changed data.
  ----------------------------------------------------------------------------------------------------------------

### FDVO vs. ODVO

-   **FDVO (`Part1FDVO`)**: Carries form or screen data, including
    values entered or selected by the user during validation.
-   **ODVO (`Part1ODVO`)**: Carries operational data retrieved from the
    system or database.

In this implementation, the current MGA ID is read from the ODVO, while
the signature status and BGA number are read from the FDVO.

------------------------------------------------------------------------

## 4. Proposed code for `DataService2Bean.java`

Remove the obsolete `MGAIdVerification` field, getter, setter, and old
`checkAndUpdateMgaId(...)` method as applicable. Add the following
method and helper method to `DataService2Bean.java`.

``` java
/**
 * ADO 1036196
 * Update MGAID_TXT for SOP documents in an independent transaction.
 */
@TransactionAttribute(value = TransactionAttributeType.REQUIRES_NEW)
public Boolean updateMgaIdForSopDocuments(String caseId, String targetMgaId)
        throws CaseServiceException {

    long startPerfTime = com.gefa.genius.perf.PerfMonitor.getStartTime();
    IFLog dsLogger = DSLogger.getLogger("Case", caseId);

    try {
        if (targetMgaId == null) {
            return Boolean.FALSE;
        }

        CommonFactory commonFactory = CommonFactory.getHandle();
        Docmt_instncFactory docmtInstncFac =
                (Docmt_instncFactory) commonFactory.createFactory("Docmt_instnc");

        Collection docList = docmtInstncFac.findByCasenbr(caseId);

        if (docList != null && !docList.isEmpty()) {
            Iterator it = docList.iterator();

            while (it.hasNext()) {
                Docmt_instnc docmtInstnc = (Docmt_instnc) PortableRemoteObject.narrow(
                        it.next(), Docmt_instnc.class);

                Docmt_instncData docmtInstncData =
                        docmtInstnc.getDocmt_instncData();

                if (docmtInstncData == null) {
                    continue;
                }

                Long evdnceTyCd = docmtInstncData.getEvdnce_ty_cd();

                if (isSopDocument(evdnceTyCd)) {
                    docmtInstncData.setMgaid_txt(targetMgaId);
                    docmtInstnc.setDocmt_instncData(docmtInstncData);
                }
            }
        }

        com.gefa.genius.perf.PerfMonitor.writeExecTime(
                startPerfTime,
                "DataServicesEJB::DataService2Bean::updateMgaIdForSopDocuments::1");

        return Boolean.TRUE;

    } catch (Exception ex) {
        dsLogger.moduleDebug(
                "Exception in updateMgaIdForSopDocuments: " + ex.getMessage(),
                IFLog.ERROR);

        throw new CaseServiceException(ex);
    }
}

private boolean isSopDocument(Long evdnceTyCd) {
    if (evdnceTyCd == null) {
        return false;
    }

    return DSConstants.EVDNCE_TYPART1.equals(evdnceTyCd)
            || DSConstants.EVDNCE_TYHIVCONSENT.equals(evdnceTyCd)
            || DSConstants.EVDNCE_TYREPLACEMENTFORM.equals(evdnceTyCd)
            || DSConstants.EVDNCE_TYTIAAREPORT.equals(evdnceTyCd)
            || DSConstants.EVDNCE_TYPAYMENTAUTH.equals(evdnceTyCd)
            || DSConstants.EVDNCE_TYFINANCIALSUPPLEMENT.equals(evdnceTyCd)
            || DSConstants.EVDNCE_TYRESIDENTALIENSUPPLEMENT.equals(evdnceTyCd);
}
```

### Before compiling, verify imports and project conventions

Confirm that the file already imports, or add the correct
project-specific imports for:

-   `TransactionAttribute`
-   `TransactionAttributeType`
-   `PortableRemoteObject`
-   `Collection`
-   `Iterator`
-   `CommonFactory`
-   `Docmt_instncFactory`
-   `Docmt_instnc`
-   `Docmt_instncData`
-   `DSConstants`
-   `CaseServiceException`
-   `IFLog` and `DSLogger`

Use the existing imports and package conventions in the project rather
than assuming package names.

> **Implementation checks:** Confirm that `findByCasenbr(caseId)`
> returns the expected remote references, that the entity setter
> persists changes in this application, and that the seven evidence-type
> constants are the correct SOP document types. Also confirm the
> intended behavior for a blank `targetMgaId`, a case with no matching
> documents, and exceptions. The sample currently checks only for
> `null`, and returns `TRUE` even when no documents are found.

------------------------------------------------------------------------

## 5. Five-file Eclipse verification checklist

### 1. `GetPart1ODVO.java`

-   [ ] Only one `//v1.0.20` block exists.
-   [ ] The `DOCMT_INSTNC` lookup for the Part 1 evidence type is
    present.
-   [ ] The retrieved `mgaid_txt` is assigned using
    `part1ODVO.setMgaIDCd(...)`.
-   [ ] The block is placed immediately before `return part1ODVO;`.
-   [ ] No later statement overwrites the assigned MGA ID.

### 2. `DataService2.java`

-   [ ] The old `checkAndUpdateMgaId(...)` declaration is removed or
    updated as required.
-   [ ] The interface declares:

``` java
updateMgaIdForSopDocuments(String caseId, String targetMgaId)
```

-   [ ] The `getMgaIdByBgaAndSignType(...)` declaration remains
    available.

### 3. `DataService2AccessBean.java`

-   [ ] `getMgaIdByBgaAndSignType(...)` delegates to:

``` java
getEjbRef().getMgaIdByBgaAndSignType(...)
```

-   [ ] There is no placeholder `return null;` implementation.
-   [ ] `updateMgaIdForSopDocuments(...)` delegates to the corresponding
    `getEjbRef()` method.
-   [ ] Method signatures and checked exceptions match the
    `DataService2` interface and bean implementation.

### 4. `DataService2Bean.java`

-   [ ] Remove `private transient MGAIdVerification mGAIdVerification;`.
-   [ ] Remove `setMGAIdVerification(...)`.
-   [ ] Remove `getMGAIdVerification(...)`.
-   [ ] Remove the obsolete `checkAndUpdateMgaId(...)` implementation if
    no longer used.
-   [ ] Add `updateMgaIdForSopDocuments(...)`.
-   [ ] Add the `isSopDocument(...)` helper.
-   [ ] Confirm
    `@TransactionAttribute(TransactionAttributeType.REQUIRES_NEW)` is
    applied to the update method.
-   [ ] Confirm all imports and method signatures compile.

### 5. `Part1FormValidation.java`

-   [ ] Call `checkAndUpdateMGAIDCD(...)` immediately after the
    `part1ODVO == null` check.
-   [ ] Read the current MGA ID from `part1ODVO.getMgaIDCd()`.
-   [ ] Return without updating if the current MGA ID is not
    `"GENPACT"`.
-   [ ] Read the signature description from the FDVO.
-   [ ] Convert the description using `VOUtilsCdForDescriptionForAV`.
-   [ ] Read the BGA number from the managing agency report FDVO for the
    e-signed branch.
-   [ ] Call `dsBean2.getMgaIdByBgaAndSignType(...)` for the configured
    MGA ID.
-   [ ] Apply the `"NBS"` and `"EPB"` fallback rules as specified by the
    business requirement.
-   [ ] Call `dsBean2.updateMgaIdForSopDocuments(caseId, targetMgaId)`.
-   [ ] Update the in-memory ODVO using
    `part1ODVO.setMgaIDCd(targetMgaId)` after the database update
    succeeds.

------------------------------------------------------------------------

## 6. Suggested test scenarios

  -----------------------------------------------------------------------
  Scenario                            Expected result
  ----------------------------------- -----------------------------------
  Current MGA ID is not `GENPACT`     No MGA ID update is performed.

  Current MGA ID is `GENPACT` and     Target MGA ID is `NBS`; eligible
  signature is not e-signed           SOP documents are updated.

  Current MGA ID is `GENPACT` and     The configured MGA ID is used.
  signature is e-signed with a        
  matching BGA/signature              
  configuration                       

  Current MGA ID is `GENPACT` and the Target MGA ID falls back to `EPB`.
  BGA/signature lookup returns null   
  or blank                            

  A document has an evidence type     That document's MGA ID is not
  outside the seven SOP types         changed.

  A document's data object is null    That document is skipped.

  No documents are returned for the   Method follows the agreed
  case                                no-document behavior; verify
                                      whether `TRUE` is appropriate.

  The document update throws an       The method logs the exception and
  exception                           throws `CaseServiceException`.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 7. Important review points

This document describes the proposed implementation based on the
supplied code and explanation. Before committing the change, validate
these points against the actual GENIUS codebase and project conventions:

1.  **Transaction behavior:** `REQUIRES_NEW` commits independently only
    if the method is invoked through the EJB container proxy and the
    transaction completes successfully. Check whether this independent
    commit is genuinely required by the business requirement.
2.  **Entity persistence:** Confirm that calling
    `setDocmt_instncData(...)` on the remote entity bean persists the
    modified `MGAID_TXT` field in this application.
3.  **Failure handling:** If the database update fails, do not update
    the in-memory ODVO as though persistence succeeded.
4.  **Return value:** Decide whether no matching documents should return
    `TRUE`, `FALSE`, or a distinct result. The sample currently returns
    `TRUE` when the query returns no documents.
5.  **Null and blank handling:** The sample checks
    `targetMgaId == null`; decide whether blank or whitespace-only
    values must also be rejected.
6.  **Legacy references:** Search the entire workspace for
    `MGAIdVerification`, `setMGAIdVerification`, `getMGAIdVerification`,
    and `checkAndUpdateMgaId` before removing old code.
7.  **Constants and evidence types:** Verify the seven `DSConstants`
    values against the approved SOP document list.
