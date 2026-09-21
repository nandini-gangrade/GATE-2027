# GATE 2027 — PERCENTAGE COMPLETE NOTES

> **Purpose:** GATE Aptitude preparation
>
> **Format:** GitHub-compatible Markdown
>
> **Focus:** Concepts, formulas, mental shortcuts, tricky questions, and common mistakes.

---

# 📑 Table of Contents

1. [Percentage Basics](#1-percentage-basics)
2. [Calculating Percentage of a Quantity](#2-calculating-percentage-of-a-quantity)
3. [Fraction–Decimal–Percentage Conversions](#3-fractiondecimalpercentage-conversions)
4. [Fraction Families and Numerator Tricks](#4-fraction-families-and-numerator-tricks)
5. [Percentage Multipliers](#5-percentage-multipliers)
6. [Percentage Increase and Decrease](#6-percentage-increase-and-decrease)
7. [Decimal Multipliers and Percentage Change](#7-decimal-multipliers-and-percentage-change)
8. [Percentage Change vs Percentage Difference](#8-percentage-change-vs-percentage-difference)
9. [Successive Percentage Changes](#9-successive-percentage-changes)
10. [Finding the Original Value](#10-finding-the-original-value)
11. [More Than and Less Than](#11-more-than-and-less-than)
12. [Percentage Applications in GATE](#12-percentage-applications-in-gate)
13. [Profit, Loss, Discount, and Tax](#13-profit-loss-discount-and-tax)
14. [Ratios and Percentages](#14-ratios-and-percentages)
15. [Population and Growth Problems](#15-population-and-growth-problems)
16. [Common GATE Traps](#16-common-gate-traps)
17. [Practice Questions](#17-practice-questions)
18. [Practice Answers](#18-practice-answers)

---

# 🧠 QUICK REVISION ROADMAP

Use this page for last-minute revision.

| Concept                      | Formula / Shortcut               | Example                          |
| ---------------------------- | -------------------------------- | -------------------------------- |
| Calculate percentage         | `(Part / Whole) × 100`           | 30 out of 120 = 25%              |
| Calculate a value            | `(Percentage / 100) × Total`     | 25% of 800 = 200                 |
| Find the whole               | `Part × 100 / Percentage`        | 200 is 25% of 800                |
| Increase by x%               | `Original × (1 + x/100)`         | 500 × 1.2 = 600                  |
| Decrease by x%               | `Original × (1 − x/100)`         | 500 × 0.8 = 400                  |
| Find original after increase | `New / (1 + x/100)`              | 600 / 1.2 = 500                  |
| Find original after decrease | `New / (1 − x/100)`              | 400 / 0.8 = 500                  |
| Decimal > 1                  | `(Decimal − 1) × 100` = increase | 1.25 = 25% increase              |
| Decimal < 1                  | `(1 − Decimal) × 100` = decrease | 0.75 = 25% decrease              |
| Two successive changes       | `a + b + ab/100`                 | 20%, then 10% = 32% increase     |
| Same increase and decrease   | `x²/100` = net loss              | 20% up, 20% down = 4% loss       |
| More → less conversion       | `x/(100 + x) × 100`              | 25% more = 20% less              |
| Less → more conversion       | `x/(100 − x) × 100`              | 20% less = 25% more              |
| Percentage difference        | `Difference / Reference × 100`   | 20/100 × 100 = 20%               |
| Percentage points            | `New rate − Old rate`            | 30% − 20% = 10 percentage points |
| Profit percentage            | `Profit / Cost Price × 100`      | Profit 100 on CP 500 = 20%       |
| Discount percentage          | `Discount / Marked Price × 100`  | Discount 100 on MP 500 = 20%     |

---

# 1. PERCENTAGE BASICS

## 1.1 What does percentage mean?

The word **percentage** means **per hundred**.

For example:

```text
25% = 25 out of 100
   = 25/100
   = 1/4
   = 0.25
```

### Basic formula

```text
Percentage = (Part / Whole) × 100
```

### Example

A student answers 45 questions correctly out of 60.

Find the percentage of correct answers.

```text
Percentage = (45 / 60) × 100
           = 75%
```

**Answer: 75%**

### Mental shortcut

Always ask:

> "Percentage of what?"

The denominator is the **reference quantity**.

For example:

```text
20 is what percentage of 50?

Answer = (20 / 50) × 100
       = 40%
```

But:

```text
20 is what percentage of 100?

Answer = (20 / 100) × 100
       = 20%
```

The same number can represent different percentages depending on the reference.

---

# 2. CALCULATING THE PERCENTAGE OF A QUANTITY

## 2.1 Formula: Find a value when the percentage is given

Use this when the question asks:

* Find 20% of 500.
* Calculate 12.5% of 800.
* What is 35% of 240?

### Formula

```text
Required value = (Percentage / 100) × Total value
```

### Example 1: Find 20% of 600

```text
Required value = (20 / 100) × 600
               = 120
```

**Answer: 120**

### Example 2: Find 12.5% of 800

We know:

```text
12.5% = 1/8
```

Therefore:

```text
12.5% of 800 = 800 / 8
             = 100
```

**Answer: 100**

### Mental shortcuts

| Percentage           | Shortcut                        |
| -------------------- | ------------------------------- |
| 10%                  | Divide by 10                    |
| 1%                   | Divide by 100                   |
| 5%                   | Half of 10%                     |
| 20%                  | Divide by 5                     |
| 25%                  | Divide by 4                     |
| 50%                  | Divide by 2                     |
| 12.5%                | Divide by 8                     |
| 33.33% approximately | Divide by 3                     |
| 66.67% approximately | Multiply by 2, then divide by 3 |
| 75%                  | Multiply by 3, then divide by 4 |

### Example 3: Find 35% of 240 mentally

```text
35% = 30% + 5%

30% of 240 = 72
5% of 240 = 12

35% of 240 = 72 + 12
           = 84
```

**Answer: 84**

---

## 2.2 Formula: Find the total value

Use this when the question says:

> 30 is 15% of what number?

### Formula

```text
Total value = (Part × 100) / Percentage
```

### Example

30 is 15% of a number. Find the number.

```text
Total = (30 × 100) / 15
      = 200
```

**Answer: 200**

### Mental shortcut

If 15% = 30:

```text
5% = 10
100% = 200
```

---

# 3. FRACTION–DECIMAL–PERCENTAGE CONVERSIONS

## 3.1 The three basic conversion formulas

```text
Percentage = Fraction × 100
```

```text
Decimal = Percentage / 100
```

```text
Fraction = Percentage / 100
```

After converting to a fraction, simplify it.

### Example

Convert 40% into a fraction and decimal.

```text
Fraction = 40/100
         = 2/5

Decimal = 40/100
        = 0.4
```

Therefore:

```text
40% = 2/5 = 0.4
```

---

## 3.2 Important fraction–percentage table

These values are extremely useful for mental calculations.

| Fraction |     Decimal |  Percentage |
| -------- | ----------: | ----------: |
| 1/2      |         0.5 |         50% |
| 1/3      |   0.3333... |   33.33...% |
| 1/4      |        0.25 |         25% |
| 1/5      |         0.2 |         20% |
| 1/6      |   0.1666... |   16.66...% |
| 1/7      | 0.142857... | 14.2857...% |
| 1/8      |       0.125 |       12.5% |
| 1/9      |   0.1111... |   11.11...% |
| 1/10     |         0.1 |         10% |
| 2/3      |   0.6666... |   66.66...% |
| 3/4      |        0.75 |         75% |
| 2/5      |         0.4 |         40% |
| 3/5      |         0.6 |         60% |
| 5/8      |       0.625 |       62.5% |

> **Important:** Values such as 33.33% and 16.67% are rounded approximations. In exact calculations, use 1/3 and 1/6 instead of their rounded percentages.

---

# 4. FRACTION FAMILIES AND NUMERATOR TRICKS

This section helps you quickly recognize fractions from percentages.

## 4.1 The basic idea

Suppose:

```text
1/8 = 12.5%
```

Then:

```text
2/8 = 25%
3/8 = 37.5%
4/8 = 50%
5/8 = 62.5%
6/8 = 75%
7/8 = 87.5%
8/8 = 100%
```

### The trick

> **Denominator = Total number of equal pieces.**
>
> **Numerator = Number of pieces taken.**

To find the numerator:

```text
Numerator = Given percentage / Percentage of one piece
```

### Example

Convert 62.5% into a fraction.

We know:

```text
1/8 = 12.5%
```

Therefore:

```text
Numerator = 62.5 / 12.5
          = 5
```

So:

```text
62.5% = 5/8
```

---

## 4.2 Eighths family

Base value:

```text
1/8 = 12.5%
```

| Percentage | Fraction | Simplified fraction |
| ---------: | -------: | ------------------: |
|      12.5% |      1/8 |                 1/8 |
|        25% |      2/8 |                 1/4 |
|      37.5% |      3/8 |                 3/8 |
|        50% |      4/8 |                 1/2 |
|      62.5% |      5/8 |                 5/8 |
|        75% |      6/8 |                 3/4 |
|      87.5% |      7/8 |                 7/8 |
|       100% |      8/8 |                   1 |

### Mental trick

To find the numerator:

```text
Numerator = Percentage / 12.5
```

Example:

```text
37.5 / 12.5 = 3

Therefore, 37.5% = 3/8
```

### Complement trick

The complementary fractions add up to 1.

```text
3/8 + 5/8 = 1
```

Therefore:

```text
37.5% + 62.5% = 100%
```

If you remember 3/8, you can instantly find 5/8.

---

## 4.3 Sixths family

Base value:

```text
1/6 = 16.666...%
```

| Percentage | Sixth-family fraction | Simplified fraction |
| ---------: | --------------------: | ------------------: |
|     16.67% |                   1/6 |                 1/6 |
|     33.33% |                   2/6 |                 1/3 |
|        50% |                   3/6 |                 1/2 |
|     66.67% |                   4/6 |                 2/3 |
|     83.33% |                   5/6 |                 5/6 |
|       100% |                   6/6 |                   1 |

### Why does 66.67% appear in the sixths family?

Because:

```text
4/6 = 2/3
```

Therefore:

```text
66.67% ≈ 2/3 = 4/6
```

The same percentage can belong to multiple families.

### Mental trick

```text
Numerator = Percentage / 16.666...
```

For practical calculations, it is easier to remember the sequence:

```text
1/6 → 16.67%
2/6 → 33.33%
3/6 → 50%
4/6 → 66.67%
5/6 → 83.33%
```

---

## 4.4 Fifths family

Base value:

```text
1/5 = 20%
```

| Percentage | Fraction | Simplified fraction |
| ---------: | -------: | ------------------: |
|        20% |      1/5 |                 1/5 |
|        40% |      2/5 |                 2/5 |
|        60% |      3/5 |                 3/5 |
|        80% |      4/5 |                 4/5 |
|       100% |      5/5 |                   1 |

### Mental trick

```text
Numerator = Percentage / 20
```

Example:

```text
60 / 20 = 3

Therefore, 60% = 3/5
```

---

## 4.5 Quarters family

Base value:

```text
1/4 = 25%
```

| Percentage | Fraction | Simplified fraction |
| ---------: | -------: | ------------------: |
|        25% |      1/4 |                 1/4 |
|        50% |      2/4 |                 1/2 |
|        75% |      3/4 |                 3/4 |
|       100% |      4/4 |                   1 |

### Mental trick

```text
Numerator = Percentage / 25
```

Example:

```text
75 / 25 = 3

Therefore, 75% = 3/4
```

---

## 4.6 Thirds family

Base value:

```text
1/3 = 33.333...%
```

| Percentage | Fraction | Simplified fraction |
| ---------: | -------: | ------------------: |
|     33.33% |      1/3 |                 1/3 |
|     66.67% |      2/3 |                 2/3 |
|       100% |      3/3 |                   1 |

### Mental trick

```text
1/3 ≈ 33.33%
2/3 ≈ 66.67%
```

Example:

```text
66.67% ≈ 2/3
```

---

## 4.7 Tenths family

Base value:

```text
1/10 = 10%
```

| Percentage |   Fraction |
| ---------: | ---------: |
|        10% |       1/10 |
|        20% | 2/10 = 1/5 |
|        30% |       3/10 |
|        40% | 4/10 = 2/5 |
|        50% | 5/10 = 1/2 |
|        60% | 6/10 = 3/5 |
|        70% |       7/10 |
|        80% | 8/10 = 4/5 |
|        90% |       9/10 |
|       100% |          1 |

### Mental trick

```text
Numerator = Percentage / 10
```

---

## 4.8 Twentieths family

Base value:

```text
1/20 = 5%
```

| Percentage |     Fraction |
| ---------: | -----------: |
|         5% |         1/20 |
|        10% |  2/20 = 1/10 |
|        15% |         3/20 |
|        20% |   4/20 = 1/5 |
|        25% |   5/20 = 1/4 |
|        30% |  6/20 = 3/10 |
|        35% |         7/20 |
|        40% |   8/20 = 2/5 |
|        45% |         9/20 |
|        50% |  10/20 = 1/2 |
|        55% |        11/20 |
|        60% |  12/20 = 3/5 |
|        65% |        13/20 |
|        70% | 14/20 = 7/10 |
|        75% |  15/20 = 3/4 |
|        80% |  16/20 = 4/5 |
|        85% |        17/20 |
|        90% | 18/20 = 9/10 |
|        95% |        19/20 |
|       100% |            1 |

### Mental trick

```text
Numerator = Percentage / 5
```

Example:

```text
35 / 5 = 7

Therefore, 35% = 7/20
```

---

## 4.9 Other useful fraction families

You can construct any family using the same rule.

| Denominator | One piece | Percentage sequence                                                  |
| ----------: | --------: | -------------------------------------------------------------------- |
|           2 |       50% | 50%, 100%                                                            |
|           3 |    33.33% | 33.33%, 66.67%, 100%                                                 |
|           4 |       25% | 25%, 50%, 75%, 100%                                                  |
|           5 |       20% | 20%, 40%, 60%, 80%, 100%                                             |
|           6 |    16.67% | 16.67%, 33.33%, 50%, 66.67%, 83.33%, 100%                            |
|           7 |    14.29% | 14.29%, 28.57%, 42.86%, 57.14%, 71.43%, 85.71%, 100%                 |
|           8 |     12.5% | 12.5%, 25%, 37.5%, 50%, 62.5%, 75%, 87.5%, 100%                      |
|           9 |    11.11% | 11.11%, 22.22%, 33.33%, 44.44%, 55.56%, 66.67%, 77.78%, 88.89%, 100% |
|          10 |       10% | 10%, 20%, 30%, ..., 100%                                             |

### General formula

If one piece is:

```text
1/n = p%
```

Then:

```text
k/n = k × p%
```

provided that `k` is between 1 and `n`.

---

# 5. PERCENTAGE MULTIPLIERS

Multipliers are one of the most useful tools in GATE aptitude.

Instead of calculating the percentage separately, we directly multiply the original value by a number.

---

## 5.1 Why does a multiplier work?

Suppose your salary is ₹500 and it increases by 20%.

The original salary represents 100%.

After the increase:

```text
New percentage = 100% + 20%
              = 120%
```

Convert 120% to a decimal:

```text
120 / 100 = 1.2
```

Therefore:

```text
New salary = 500 × 1.2
           = ₹600
```

The multiplier `1.2` already includes the original value and the increase.

---

## 5.2 Formula: Percentage increase multiplier

Use this when a value increases by a given percentage.

```text
Increase multiplier = 1 + (Increase percentage / 100)
```

```text
New value = Original value × Increase multiplier
```

### Examples

| Increase | Calculation  | Multiplier |
| -------: | ------------ | ---------: |
|       4% | 1 + 4/100    |       1.04 |
|      10% | 1 + 10/100   |       1.10 |
|    12.5% | 1 + 12.5/100 |      1.125 |
|      20% | 1 + 20/100   |       1.20 |
|      25% | 1 + 25/100   |       1.25 |
|      36% | 1 + 36/100   |       1.36 |
|      50% | 1 + 50/100   |       1.50 |
|     100% | 1 + 100/100  |          2 |

### Example

A number is increased by 36%. Find the new value if the original value is 250.

```text
Multiplier = 1 + 36/100
           = 1.36

New value = 250 × 1.36
          = 340
```

**Answer: 340**

---

## 5.3 Formula: Percentage decrease multiplier

Use this when a value decreases by a given percentage.

```text
Decrease multiplier = 1 − (Decrease percentage / 100)
```

```text
New value = Original value × Decrease multiplier
```

### Examples

| Decrease | Calculation  | Multiplier |
| -------: | ------------ | ---------: |
|       4% | 1 − 4/100    |       0.96 |
|      10% | 1 − 10/100   |       0.90 |
|    12.5% | 1 − 12.5/100 |      0.875 |
|      20% | 1 − 20/100   |       0.80 |
|      25% | 1 − 25/100   |       0.75 |
|      36% | 1 − 36/100   |       0.64 |
|      50% | 1 − 50/100   |       0.50 |
|      75% | 1 − 75/100   |       0.25 |

### Example

A value of 800 decreases by 25%.

```text
Multiplier = 1 − 25/100
           = 0.75

New value = 800 × 0.75
          = 600
```

**Answer: 600**

---

## 5.4 Constructing multipliers using fractions

This is useful when you know fraction–percentage conversions.

### Example 1: Increase by 12.5%

We know:

```text
12.5% = 1/8
```

Therefore:

```text
Increase multiplier = 1 + 1/8
                    = (8 + 1)/8
                    = 9/8
```

So:

```text
12.5% increase = ×9/8
```

#### Example

Increase 800 by 12.5%.

```text
New value = 800 × 9/8
          = 100 × 9
          = 900
```

**Answer: 900**

---

### Example 2: Decrease by 12.5%

We know:

```text
12.5% = 1/8
```

Therefore:

```text
Decrease multiplier = 1 − 1/8
                    = (8 − 1)/8
                    = 7/8
```

So:

```text
12.5% decrease = ×7/8
```

#### Example

Decrease 800 by 12.5%.

```text
New value = 800 × 7/8
          = 100 × 7
          = 700
```

**Answer: 700**

---

# 6. PERCENTAGE INCREASE AND DECREASE

## 6.1 Formula: Calculate percentage change

Use this when a quantity changes from an initial value to a final value.

```text
Percentage change = ((Final value − Initial value) / Initial value) × 100
```

Interpretation:

* Positive result = percentage increase.
* Negative result = percentage decrease.
* Zero = no change.

### Example 1: Percentage increase

A value increases from 200 to 250.

```text
Percentage change = ((250 − 200) / 200) × 100
                  = (50 / 200) × 100
                  = 25%
```

**Answer: 25% increase**

### Example 2: Percentage decrease

A value decreases from 200 to 150.

```text
Percentage change = ((150 − 200) / 200) × 100
                  = −25%
```

**Answer: 25% decrease**

### Important correction

You may also see the formula written as:

```text
Percentage decrease = ((Initial − Final) / Initial) × 100
```

Both forms are valid when used correctly.

For a general signed change, use:

```text
(Final − Initial) / Initial × 100
```

---

## 6.2 How to calculate the increase or decrease directly

### Example

A machine produces 800 units. Its production increases by 10%.

```text
Increase = 10% of 800
         = 80
```

```text
New production = 800 + 80
               = 880
```

Or directly:

```text
New production = 800 × 1.1
               = 880
```

---

## 6.3 Common percentage increase and decrease table

| Percentage | Increase multiplier | Decrease multiplier |
| ---------: | ------------------: | ------------------: |
|         4% |                1.04 |                0.96 |
|         5% |                1.05 |                0.95 |
|        10% |                1.10 |                0.90 |
|      12.5% |               1.125 |               0.875 |
|        20% |                1.20 |                0.80 |
|        25% |                1.25 |                0.75 |
|        30% |                1.30 |                0.70 |
|        36% |                1.36 |                0.64 |
|        50% |                1.50 |                0.50 |
|        75% |                1.75 |                0.25 |
|       100% |                2.00 |                0.00 |

### Mental rule

```text
Multiplier > 1 → Increase
Multiplier < 1 → Decrease
Multiplier = 1 → No change
```

---

# 7. DECIMAL MULTIPLIERS AND PERCENTAGE CHANGE

## 7.1 Formula: Decimal multiplier to percentage increase

Use this when a question says:

> A value becomes 1.3 times its original value. Find the percentage increase.

```text
Percentage increase = (Multiplier − 1) × 100
```

### Example

A machine's output becomes 1.36 times its original output.

```text
Percentage increase = (1.36 − 1) × 100
                   = 36%
```

**Answer: 36% increase**

---

## 7.2 Formula: Decimal multiplier to percentage decrease

Use this when a value becomes less than its original value.

```text
Percentage decrease = (1 − Multiplier) × 100
```

### Example 1

A value becomes 0.7 times its original value.

```text
Percentage decrease = (1 − 0.7) × 100
                   = 30%
```

**Answer: 30% decrease**

### Example 2

A value becomes 0.67 times its original value.

```text
Percentage decrease = (1 − 0.67) × 100
                   = 33%
```

**Answer: 33% decrease**

### Example 3

A value becomes 0.956 times its original value.

```text
Percentage decrease = (1 − 0.956) × 100
                   = 4.4%
```

**Answer: 4.4% decrease**

### Important trap

```text
0.7 = 70% of the original value
```

It does **not** mean a 70% decrease.

The decrease is:

```text
100% − 70% = 30%
```

---

# 8. PERCENTAGE CHANGE VS PERCENTAGE DIFFERENCE

These concepts are often confused.

---

## 8.1 Percentage change

Use this when comparing a value before and after a change.

### Formula

```text
Percentage change = ((Final − Initial) / Initial) × 100
```

The initial value is the reference.

### Example

A price increases from ₹80 to ₹100.

```text
Percentage increase = ((100 − 80) / 80) × 100
                   = 25%
```

**Answer: 25% increase**

---

## 8.2 Percentage difference

Use this when comparing two values and the question specifies a reference value.

### Formula

```text
Percentage difference = (Absolute difference / Reference value) × 100
```

```text
Absolute difference = |Value 1 − Value 2|
```

### Example

Two values are 80 and 100.

The difference is:

```text
Difference = 100 − 80
           = 20
```

If the reference value is 100:

```text
Percentage difference = (20 / 100) × 100
                      = 20%
```

**Answer: 20%**

### Important distinction

If the reference is 80:

```text
Percentage difference = (20 / 80) × 100
                      = 25%
```

The result changes because the reference changes.

> Always identify the denominator before calculating a percentage.

---

## 8.3 Percentage points vs percentage change

This is a common trap.

Suppose an interest rate increases from 20% to 30%.

### Change in percentage points

```text
Percentage-point change = 30% − 20%
                        = 10 percentage points
```

### Relative percentage increase

```text
Percentage increase = ((30 − 20) / 20) × 100
                    = 50%
```

Therefore:

```text
20% → 30%

Change = 10 percentage points
Relative increase = 50%
```

These are not the same.

---

# 9. SUCCESSIVE PERCENTAGE CHANGES

Successive changes occur when a quantity changes multiple times.

Examples:

* Salary increases by 20% and then by 10%.
* Price decreases by 10% and then increases by 20%.
* Population increases by 15% for two consecutive years.

---

## 9.1 Safest formula: Multiply the multipliers

Use this for any number of successive changes.

```text
Final value = Initial value × Multiplier 1 × Multiplier 2 × ...
```

### Example

A value of 1,000 increases by 20% and then decreases by 10%.

First change:

```text
Multiplier 1 = 1.2
```

Second change:

```text
Multiplier 2 = 0.9
```

Therefore:

```text
Final value = 1000 × 1.2 × 0.9
            = 1080
```

Net change:

```text
Net change = 1080 − 1000
           = 80
```

```text
Net percentage change = (80 / 1000) × 100
                     = 8%
```

**Answer: 8% increase**

---

## 9.2 Shortcut formula for two successive changes

For two successive percentage changes of `a%` and `b%`:

```text
Net percentage change = a + b + (ab / 100)
```

Here, use signs:

* Increase = positive.
* Decrease = negative.

### Example 1: Two increases

A value increases by 20% and then by 10%.

```text
a = 20
b = 10

Net change = 20 + 10 + (20 × 10)/100
           = 30 + 2
           = 32%
```

**Answer: 32% increase**

### Example 2: Increase followed by decrease

A value increases by 20% and then decreases by 10%.

```text
a = 20
b = −10

Net change = 20 − 10 + (20 × −10)/100
           = 10 − 2
           = 8%
```

**Answer: 8% increase**

### Example 3: Two decreases

A value decreases by 20% and then by 10%.

```text
a = −20
b = −10

Net change = −20 − 10 + ((−20) × (−10))/100
           = −30 + 2
           = −28%
```

**Answer: 28% decrease**

---

## 9.3 Same percentage increase and decrease

Suppose a value increases by `x%` and then decreases by `x%`.

### Formula

```text
Net loss = x² / 100
```

### Example

A value increases by 20% and then decreases by 20%.

```text
Net loss = 20² / 100
         = 400 / 100
         = 4%
```

**Answer: 4% decrease**

### Multiplier method

```text
Final multiplier = 1.2 × 0.8
                 = 0.96
```

Only 96% remains.

```text
Loss = 100% − 96%
     = 4%
```

### Why isn't the net change zero?

Suppose the original value is 100.

After a 20% increase:

```text
100 × 1.2 = 120
```

After a 20% decrease:

```text
120 × 0.8 = 96
```

The final value is 96, not 100.

The second 20% is calculated on 120, not on the original 100.

---

## 9.4 Three or more successive changes

Use the multiplier method.

### Example

A quantity increases by 10%, then by 20%, and finally decreases by 30%.

```text
Final multiplier = 1.1 × 1.2 × 0.7
                 = 0.924
```

Therefore:

```text
Net change = (0.924 − 1) × 100
           = −7.6%
```

**Answer: 7.6% decrease**

### Important trap

Do not simply add:

```text
10 + 20 − 30 = 0
```

That would be incorrect because the changes are applied to different values.

---

## 9.5 Successive discounts

Successive discounts follow the same multiplier rule.

### Example

A product has two successive discounts of 20% and 10%.

```text
Final multiplier = 0.8 × 0.9
                 = 0.72
```

The customer pays 72% of the marked price.

```text
Equivalent discount = 100% − 72%
                    = 28%
```

**Answer: 28% equivalent discount**

---

# 10. FINDING THE ORIGINAL VALUE

This is an important GATE question type.

Use this when the final value is given and you need to find the value before a percentage change.

---

## 10.1 Formula: Original value after an increase

If a value increases by `r%`:

```text
New value = Original value × (1 + r/100)
```

Therefore:

```text
Original value = New value / (1 + r/100)
```

### Example

A number increases by 20% and becomes 600. Find the original number.

### Step 1: Find the multiplier

```text
Multiplier = 1 + 20/100
           = 1.2
```

### Step 2: Divide by the multiplier

```text
Original = 600 / 1.2
         = 6000 / 12
         = 500
```

**Answer: 500**

### Mental shortcut: Percentage method

After a 20% increase:

```text
120% = 600
```

Therefore:

```text
100% = (600 × 100) / 120
     = 500
```

---

## 10.2 Formula: Original value after a decrease

If a value decreases by `r%`:

```text
New value = Original value × (1 − r/100)
```

Therefore:

```text
Original value = New value / (1 − r/100)
```

### Example

A number decreases by 20% and becomes 480. Find the original number.

```text
Multiplier = 1 − 20/100
           = 0.8
```

```text
Original = 480 / 0.8
         = 4800 / 8
         = 600
```

**Answer: 600**

### Mental shortcut

After a 20% decrease:

```text
80% = 480
```

Therefore:

```text
100% = (480 × 100) / 80
     = 600
```

---

## 10.3 Reverse percentage using fractions

This is particularly useful for mental calculations.

### Example 1: Reverse a 25% increase

A value becomes 1,000 after a 25% increase.

```text
25% increase = ×1.25
             = ×5/4
```

To reverse the change:

```text
Original = 1000 × 4/5
         = 800
```

**Answer: 800**

---

### Example 2: Reverse a 25% decrease

A value becomes 450 after a 25% decrease.

```text
25% decrease = ×0.75
             = ×3/4
```

To reverse the change:

```text
Original = 450 × 4/3
         = 600
```

**Answer: 600**

---

### Example 3: Reverse a 12.5% decrease

A value becomes 700 after a 12.5% decrease.

```text
12.5% decrease = ×7/8
```

Therefore:

```text
Original = 700 × 8/7
         = 800
```

**Answer: 800**

---

## 10.4 Reverse successive changes

Reverse the multipliers in reverse order.

### Example

A value increases by 20% and then decreases by 10%. The final value is 1,080. Find the original value.

Forward calculation:

```text
Final = Original × 1.2 × 0.9
```

Therefore:

```text
Original = 1080 / (1.2 × 0.9)
         = 1080 / 1.08
         = 1000
```

**Answer: 1,000**

### Important trap

If the value increases by 20%, do not subtract 20% from the final value to reverse it.

You must divide by `1.2`.

---

# 11. MORE THAN AND LESS THAN

This is a classic percentage trap.

The percentage changes when the reference value changes.

---

## 11.1 A is x% more than B

Suppose:

```text
A is x% more than B
```

### Formula

```text
A = B × (1 + x/100)
```

To find how much less B is than A:

```text
Percentage by which B is less than A
= [x / (100 + x)] × 100
```

### Example: A is 25% more than B

Assume:

```text
B = 100
```

Then:

```text
A = 100 + 25% of 100
  = 125
```

Now compare B with A.

```text
Difference = 125 − 100
           = 25
```

The reference is A, which is 125.

```text
Percentage decrease = (25 / 125) × 100
                    = 20%
```

Therefore:

```text
If A is 25% more than B,
B is 20% less than A.
```

### Shortcut

```text
25% more → 25/125 × 100 = 20% less
```

---

## 11.2 A is x% less than B

Suppose:

```text
A is x% less than B
```

### Formula

```text
A = B × (1 − x/100)
```

To find how much more B is than A:

```text
Percentage by which B is more than A
= [x / (100 − x)] × 100
```

### Example: A is 20% less than B

Assume:

```text
B = 100
```

Then:

```text
A = 100 − 20
  = 80
```

Difference:

```text
Difference = 100 − 80
           = 20
```

The reference is A, which is 80.

```text
Percentage increase = (20 / 80) × 100
                    = 25%
```

Therefore:

```text
If A is 20% less than B,
B is 25% more than A.
```

---

## 11.3 Quick conversion table

| Given statement       | Equivalent reverse statement |
| --------------------- | ---------------------------- |
| A is 10% more than B  | B is 9.09% less than A       |
| A is 20% more than B  | B is 16.67% less than A      |
| A is 25% more than B  | B is 20% less than A         |
| A is 50% more than B  | B is 33.33% less than A      |
| A is 100% more than B | B is 50% less than A         |
| A is 10% less than B  | B is 11.11% more than A      |
| A is 20% less than B  | B is 25% more than A         |
| A is 25% less than B  | B is 33.33% more than A      |
| A is 50% less than B  | B is 100% more than A        |

### Important trap

```text
A is 25% more than B
```

does not mean:

```text
B is 25% less than A
```

The reference values are different.

---

# 12. PERCENTAGE APPLICATIONS IN GATE

Percentage questions can appear in many forms.

---

## 12.1 Marks and examination questions

### Type 1: Find percentage marks

A student scores 72 marks out of 90.

```text
Percentage = (72 / 90) × 100
           = 80%
```

**Answer: 80%**

---

### Type 2: Find marks from percentage

A student scores 75% in an examination of 800 marks.

```text
Marks = (75 / 100) × 800
      = 600
```

**Answer: 600 marks**

---

### Type 3: Percentage increase in marks

A student's marks increase from 60 to 75.

```text
Increase = 75 − 60
         = 15
```

```text
Percentage increase = (15 / 60) × 100
                    = 25%
```

**Answer: 25% increase**

### Trap

The denominator is the original marks, not the final marks.

---

## 12.2 Income and expenditure

These questions often combine percentages with ratios.

### Example

A person's income is ₹20,000.

They spend 70% of their income.

Find their savings.

```text
Expenditure = 70% of 20000
            = 14000
```

```text
Savings = Income − Expenditure
        = 20000 − 14000
        = 6000
```

**Answer: ₹6,000**

Savings as a percentage of income:

```text
Savings percentage = (6000 / 20000) × 100
                   = 30%
```

### Important trap

If expenditure increases by 20%, savings do not necessarily decrease by 20%.

You must calculate the new expenditure and then subtract it from income.

---

## 12.3 Ratio-based percentage questions

Suppose:

```text
A : B = 3 : 5
```

### A as a percentage of B

```text
Percentage = (3 / 5) × 100
           = 60%
```

### A as a percentage of the total

Total parts:

```text
3 + 5 = 8
```

```text
Percentage = (3 / 8) × 100
           = 37.5%
```

### Important distinction

```text
A as a percentage of B = 60%
```

But:

```text
A as a percentage of total = 37.5%
```

The reference changes.

---

## 12.4 Part of a part

This type of question involves multiplying percentages.

### Example

Find 20% of 30% of 500.

First calculate 30% of 500:

```text
30% of 500 = 150
```

Then calculate 20% of 150:

```text
20% of 150 = 30
```

**Answer: 30**

### Shortcut

```text
20% × 30% = 0.2 × 0.3
          = 0.06
          = 6%
```

Therefore:

```text
6% of 500 = 30
```

### Formula

```text
x% of y% of N = (x/100) × (y/100) × N
```

---

# 13. PROFIT, LOSS, DISCOUNT, AND TAX

These topics frequently use percentage calculations.

---

## 13.1 Profit percentage

### Definitions

```text
Cost Price (CP) = Price at which an item is purchased
Selling Price (SP) = Price at which an item is sold
```

```text
Profit = Selling Price − Cost Price
```

### Formula

```text
Profit percentage = (Profit / Cost Price) × 100
```

### Example

An item is purchased for ₹800 and sold for ₹920.

```text
Profit = 920 − 800
       = 120
```

```text
Profit percentage = (120 / 800) × 100
                  = 15%
```

**Answer: 15% profit**

---

## 13.2 Loss percentage

### Formula

```text
Loss = Cost Price − Selling Price
```

```text
Loss percentage = (Loss / Cost Price) × 100
```

### Example

An item is purchased for ₹800 and sold for ₹680.

```text
Loss = 800 − 680
     = 120
```

```text
Loss percentage = (120 / 800) × 100
                = 15%
```

**Answer: 15% loss**

---

## 13.3 Discount percentage

### Definitions

```text
Marked Price (MP) = Listed price
Selling Price (SP) = Price after discount
```

```text
Discount = Marked Price − Selling Price
```

### Formula

```text
Discount percentage = (Discount / Marked Price) × 100
```

### Example

An item marked at ₹1,000 is sold for ₹800.

```text
Discount = 1000 − 800
         = 200
```

```text
Discount percentage = (200 / 1000) × 100
                    = 20%
```

**Answer: 20% discount**

---

## 13.4 Successive discounts

### Example

A product receives two discounts of 20% and 10%.

```text
First multiplier = 0.8
Second multiplier = 0.9
```

```text
Final multiplier = 0.8 × 0.9
                 = 0.72
```

The customer pays 72% of the original price.

```text
Equivalent discount = 100% − 72%
                    = 28%
```

**Answer: 28%**

---

## 13.5 Tax and GST-style calculations

### Formula: Price after tax

```text
Final price = Original price × (1 + Tax rate/100)
```

### Example

A product costs ₹1,000 before 18% tax.

```text
Final price = 1000 × 1.18
            = ₹1180
```

---

### Formula: Price before tax

If the final price includes tax:

```text
Original price = Final price / (1 + Tax rate/100)
```

### Example

A product costs ₹1,180 including 18% tax.

```text
Original price = 1180 / 1.18
               = ₹1000
```

### Trap

If tax is already included in the price, do not subtract 18% from the final price.

You must divide by `1.18`.

---

# 14. RATIOS AND PERCENTAGES

Ratios and percentages are closely related.

---

## 14.1 Convert a ratio into a percentage

If:

```text
A : B = 2 : 5
```

Then A as a percentage of B is:

```text
A/B × 100 = 2/5 × 100 = 40%
```

---

## 14.2 Percentage distribution from a ratio

Suppose three people divide money in the ratio:

```text
A : B : C = 2 : 3 : 5
```

Total parts:

```text
2 + 3 + 5 = 10
```

### A's share

```text
A's percentage = 2/10 × 100
               = 20%
```

### B's share

```text
B's percentage = 3/10 × 100
               = 30%
```

### C's share

```text
C's percentage = 5/10 × 100
               = 50%
```

---

## 14.3 Percentage change in a ratio

Suppose A increases by 20% and B increases by 10%.

Original ratio:

```text
A : B
```

New ratio:

```text
1.2A : 1.1B
```

Therefore:

```text
New ratio = 1.2/1.1 × A/B
```

### Example

Original ratio A:B = 2:3.

A increases by 20% and B increases by 10%.

```text
New ratio = (2 × 1.2) : (3 × 1.1)
          = 2.4 : 3.3
          = 8 : 11
```

**Answer: 8:11**

### Trap

If both quantities change, apply their respective multipliers before simplifying the ratio.

---

# 15. POPULATION AND GROWTH PROBLEMS

## 15.1 Population growth

### Formula

```text
New population = Original population × (1 + Growth rate/100)
```

### Example

A town has a population of 20,000. Its population increases by 15%.

```text
New population = 20000 × 1.15
               = 23000
```

**Answer: 23,000**

---

## 15.2 Population decrease

### Formula

```text
New population = Original population × (1 − Decrease rate/100)
```

### Example

A town has a population of 20,000. Its population decreases by 15%.

```text
New population = 20000 × 0.85
               = 17000
```

**Answer: 17,000**

---

## 15.3 Population growth over multiple years

### Formula

```text
Final population = Initial population × (1 + r/100)^n
```

Where:

* `r` = annual growth rate.
* `n` = number of years.

### Example

A town has a population of 10,000. It grows by 10% annually for 2 years.

```text
Final population = 10000 × (1.1)^2
                 = 10000 × 1.21
                 = 12100
```

**Answer: 12,100**

### Trap

Do not multiply the original population by 20% directly for two years.

The second year's growth is calculated on the increased population.

---

# 16. COMMON GATE TRAPS

## Trap 1: Using the wrong denominator

Question:

> A number increases from 80 to 100. Find the percentage increase.

Incorrect:

```text
20/100 × 100 = 20%
```

Correct:

```text
Percentage increase = 20/80 × 100
                    = 25%
```

The initial value is the reference.

---

## Trap 2: Assuming equal increases and decreases cancel

```text
+20% followed by −20% ≠ 0%
```

Correct result:

```text
1.2 × 0.8 = 0.96
```

Therefore:

```text
4% decrease
```

---

## Trap 3: Reversing a percentage incorrectly

A value increases by 25%.

To reverse it, do not decrease the final value by 25%.

Correct:

```text
Original = Final / 1.25
```

---

## Trap 4: Confusing percentage points with percentage change

A rate changes from 10% to 15%.

```text
Change in percentage points = 5
```

```text
Relative percentage increase = 5/10 × 100 = 50%
```

---

## Trap 5: Confusing percentage of a quantity with percentage increase

```text
A is 20% of B
```

means:

```text
A = 0.2B
```

But:

```text
A is 20% more than B
```

means:

```text
A = 1.2B
```

These are different statements.

---

## Trap 6: Confusing more than and less than

```text
A is 25% more than B
```

does not mean:

```text
B is 25% less than A
```

Correct:

```text
B is 20% less than A
```

---

## Trap 7: Rounding repeating fractions too early

```text
1/6 = 16.6666...%
```

Using 16.67% is an approximation.

For exact calculations, use:

```text
1/6
```

rather than the rounded percentage.

---

## Trap 8: Adding successive percentages

A quantity increases by 20% and then by 10%.

Incorrect:

```text
20% + 10% = 30%
```

Correct:

```text
1.2 × 1.1 = 1.32
```

Net increase:

```text
32%
```

---

## Trap 9: Tax included in the final price

If the final price includes 18% tax:

```text
Pre-tax price = Final price / 1.18
```

Do not simply subtract 18%.

---

## Trap 10: Confusing part-to-part and part-to-whole ratios

If:

```text
A : B = 3 : 5
```

Then:

```text
A as a percentage of B = 3/5 × 100 = 60%
```

But:

```text
A as a percentage of total = 3/8 × 100 = 37.5%
```

---

## Trap 11: Percentage of a negative number

Percentage calculations involving negative values require careful interpretation.

For example, if a quantity changes from `−100` to `−80`, the usual signed percentage-change formula gives:

```text
Percentage change = ((−80 − (−100)) / −100) × 100
                  = −20%
```

The numerical value decreased in magnitude by 20%, but the sign and context matter.

Always interpret the result in the context of the question.

---

## Trap 12: Division by zero

Percentage change relative to an initial value of zero is undefined.

```text
Percentage change = Change / Initial value × 100
```

If the initial value is zero, this formula cannot be used.

---

# 17. PRACTICE QUESTIONS

Try solving these without looking at the answers.

The questions cover the major percentage patterns discussed above.

---

## Basic percentage questions

### Q1. Calculate a percentage

A student scores 72 marks out of 90.

Find the percentage.

---

### Q2. Calculate a value

Find 12.5% of 960.

---

### Q3. Find the total

40 is 20% of which number?

---

### Q4. Fraction conversion

Convert 62.5% into a simplified fraction.

---

### Q5. Fraction family

Which fraction is equivalent to 66.67% approximately?

A. 2/3
B. 3/5
C. 4/5
D. 5/6

---

## Multiplier questions

### Q6. Increase

A salary of ₹800 increases by 25%.

Find the new salary.

---

### Q7. Decrease

A price of ₹1,000 decreases by 12.5%.

Find the new price.

---

### Q8. Decimal to percentage

A value becomes 0.64 times its original value.

Find the percentage change.

---

### Q9. Decimal multiplier construction

A quantity increases by 12.5%.

Express the increase multiplier as a fraction.

---

## Successive percentage questions

### Q10. Two successive increases

A quantity increases by 10% and then by 20%.

Find the net percentage increase.

---

### Q11. Increase and decrease

A quantity increases by 20% and then decreases by 20%.

Find the net percentage change.

---

### Q12. Three successive changes

A value increases by 10%, then by 20%, and then decreases by 30%.

Find the net percentage change.

---

### Q13. Successive discounts

A product receives discounts of 25% and 20%.

Find the equivalent discount.

---

## Reverse percentage questions

### Q14. Find the original value

A number increases by 25% and becomes 1,000.

Find the original number.

---

### Q15. Find the original value after a decrease

A number decreases by 20% and becomes 640.

Find the original number.

---

### Q16. Reverse a fraction-based change

A value decreases by 12.5% and becomes 700.

Find the original value.

---

## More than and less than

### Q17. Reverse comparison

A is 25% more than B.

By what percentage is B less than A?

---

### Q18. Reverse comparison

A is 20% less than B.

By what percentage is B more than A?

---

## GATE-style application questions

### Q19. Income and expenditure

A person earns ₹30,000 and spends 70% of their income.

Find their savings.

---

### Q20. Ratio and percentage

A:B = 3:5.

Find A as a percentage of the total.

---

### Q21. Part of a part

Find 30% of 40% of 500.

---

### Q22. Profit

An item is purchased for ₹800 and sold for ₹920.

Find the profit percentage.

---

### Q23. Tax

A product costs ₹1,180 including 18% tax.

Find its price before tax.

---

### Q24. Population

A town has a population of 10,000. It grows by 10% annually for 2 years.

Find the final population.

---

### Q25. Percentage points

An interest rate rises from 20% to 30%.

Find:

1. The change in percentage points.
2. The relative percentage increase.

---

# 18. PRACTICE ANSWERS

## Basic percentage answers

### Q1

```text
Percentage = 72/90 × 100
           = 80%
```

**Answer: 80%**

---

### Q2

```text
12.5% = 1/8

12.5% of 960 = 960/8
             = 120
```

**Answer: 120**

---

### Q3

```text
Total = (40 × 100) / 20
      = 200
```

**Answer: 200**

---

### Q4

```text
62.5% = 62.5/100
      = 625/1000
      = 5/8
```

**Answer: 5/8**

---

### Q5

**Answer: A. 2/3**

Because:

```text
2/3 = 66.666...%
```

---

## Multiplier answers

### Q6

```text
New salary = 800 × 1.25
           = ₹1000
```

**Answer: ₹1,000**

---

### Q7

```text
New price = 1000 × 0.875
          = ₹875
```

**Answer: ₹875**

---

### Q8

```text
Percentage decrease = (1 − 0.64) × 100
                   = 36%
```

**Answer: 36% decrease**

---

### Q9

```text
12.5% = 1/8

Increase multiplier = 1 + 1/8
                    = 9/8
```

**Answer: 9/8**

---

## Successive percentage answers

### Q10

```text
Net change = 10 + 20 + (10 × 20)/100
           = 32%
```

**Answer: 32% increase**

---

### Q11

```text
Final multiplier = 1.2 × 0.8
                 = 0.96
```

**Answer: 4% decrease**

**Trap:** Equal percentage increase and decrease do not cancel.

---

### Q12

```text
Final multiplier = 1.1 × 1.2 × 0.7
                 = 0.924
```

```text
Net change = (0.924 − 1) × 100
           = −7.6%
```

**Answer: 7.6% decrease**

---

### Q13

```text
Final multiplier = 0.75 × 0.8
                 = 0.6
```

```text
Equivalent discount = 100% − 60%
                    = 40%
```

**Answer: 40% discount**

---

## Reverse percentage answers

### Q14

```text
Original = 1000 / 1.25
         = 800
```

**Answer: 800**

---

### Q15

```text
Original = 640 / 0.8
         = 800
```

**Answer: 800**

---

### Q16

```text
12.5% decrease = 7/8

Original = 700 × 8/7
         = 800
```

**Answer: 800**

---

## More than and less than answers

### Q17

```text
A = 125, B = 100

Percentage by which B is less than A
= 25/125 × 100
= 20%
```

**Answer: 20% less**

---

### Q18

```text
B = 100, A = 80

Percentage by which B is more than A
= 20/80 × 100
= 25%
```

**Answer: 25% more**

---

## Application answers

### Q19

```text
Expenditure = 70% of 30000
            = 21000

Savings = 30000 − 21000
        = 9000
```

**Answer: ₹9,000**

---

### Q20

```text
A:B = 3:5

Total parts = 3 + 5 = 8

A's percentage = 3/8 × 100
               = 37.5%
```

**Answer: 37.5%**

---

### Q21

```text
30% of 40% of 500
= 0.3 × 0.4 × 500
= 60
```

**Answer: 60**

---

### Q22

```text
Profit = 920 − 800
       = 120

Profit percentage = 120/800 × 100
                  = 15%
```

**Answer: 15% profit**

---

### Q23

```text
Price before tax = 1180 / 1.18
                 = 1000
```

**Answer: ₹1,000**

---

### Q24

```text
Final population = 10000 × 1.1²
                 = 12100
```

**Answer: 12,100**

---

### Q25

Initial rate = 20%

Final rate = 30%

#### 1. Change in percentage points

```text
30% − 20% = 10 percentage points
```

#### 2. Relative percentage increase

```text
Percentage increase = (30 − 20)/20 × 100
                    = 50%
```

**Answers:**

```text
1. 10 percentage points
2. 50% relative increase
```

---

# 🎯 FINAL GATE REVISION STRATEGY

For percentage problems, follow this order:

```text
1. Identify the reference value.
2. Decide whether the question asks for:
   - Percentage
   - Actual value
   - Percentage change
   - Percentage difference
   - Original value
   - Successive change
3. Convert percentages into fractions or multipliers.
4. Apply the correct formula.
5. Check whether the answer makes logical sense.
```

## The five formulas to remember first

```text
1. Percentage = (Part / Whole) × 100
```

```text
2. Value = (Percentage / 100) × Total
```

```text
3. New value = Original × (1 ± Percentage/100)
```

```text
4. Original = New / Multiplier
```

```text
5. Net multiplier = Product of all individual multipliers
```

## Final mental rules

> **Percentage means per hundred.**

> **The denominator is the reference.**

> **Multiplier greater than 1 means increase.**

> **Multiplier less than 1 means decrease.**

> **Successive percentage changes must be multiplied.**

> **Equal percentage increase and decrease result in a loss.**

> **When reversing a percentage change, divide by the multiplier.**

> **Always distinguish percentage points from percentage change.**

---

*These notes cover the fundamental percentage concepts and common aptitude applications. For actual GATE preparation, supplement them with year-wise PYQs and verify the exact wording and difficulty of questions from the official papers.*
