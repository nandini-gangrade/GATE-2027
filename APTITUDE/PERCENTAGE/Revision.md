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
Percentage
