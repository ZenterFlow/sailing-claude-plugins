# Interpolation Guide for Deviation Tables

## When to Interpolate

### ✅ INTERPOLATE when:
- Compass heading falls between table entries
- Difference from nearest entry is >1°
- Precision matters for passage planning

### ❌ DON'T INTERPOLATE when:
- Heading exactly matches table entry
- Within 1° of table entry (use nearest)
- Deviation values are the same for bracketing entries

---

## Step-by-Step Interpolation Method

### The Formula

For a compass heading **H** between table entries **H₁** and **H₂** with deviations **D₁** and **D₂**:

```
Position Ratio (P) = (H - H₁) ÷ (H₂ - H₁)

Interpolated Deviation = D₁ + (P × (D₂ - D₁))
```

### Step 1: Find Bracketing Values

Identify the two table entries that surround your heading.

**Example:** Find deviation at 081°(C)

Table shows:
- 067.5° → 2°E
- 090.0° → 4°E

Bracketing values: **H₁ = 067.5°**, **H₂ = 090.0°**

---

### Step 2: Calculate Position Ratio

Determine how far your heading is between the two table entries.

```
P = (H - H₁) ÷ (H₂ - H₁)
P = (81 - 67.5) ÷ (90 - 67.5)
P = 13.5 ÷ 22.5
P = 0.60
```

**Meaning:** 081° is 60% of the way from 067.5° to 090°

---

### Step 3: Calculate Deviation Range

Find the difference between the two deviation values.

**Handle East/West carefully:**
- East = positive (+)
- West = negative (-)

```
Deviation Range = D₂ - D₁
                = 4°E - 2°E
                = +4° - (+2°)
                = 2°
```

---

### Step 4: Interpolate the Deviation

Apply the position ratio to the deviation range.

```
Interpolated Deviation = D₁ + (P × Range)
                       = 2°E + (0.60 × 2°)
                       = 2°E + 1.2°
                       = 3.2°E
```

---

### Step 5: Round Appropriately

Round to practical precision:
- **1° for general use** → 3°E
- **0.5° for precise work** → 3.0°E

**Final Answer:** Deviation at 081°(C) ≈ **3°E**

---

## Worked Examples

### Example 1: Simple Interpolation (Both East)

**Find deviation at 038°(C)**

```
Table:
  030° → 4°E
  045° → 4°E

Analysis:
  Both deviations the same!
  No interpolation needed.

Answer: 4°E
```

---

### Example 2: Different East Values

**Find deviation at 113°(C)**

```
Table:
  105° → 5°E
  120° → 4°E

Step 1: Bracketing values
  H₁ = 105°, H₂ = 120°
  D₁ = 5°E, D₂ = 4°E

Step 2: Position ratio
  P = (113 - 105) ÷ (120 - 105)
  P = 8 ÷ 15 = 0.533

Step 3: Deviation range
  Range = 4°E - 5°E = -1° (decreasing)

Step 4: Interpolate
  Deviation = 5°E + (0.533 × -1°)
           = 5°E - 0.533°
           = 4.5°E

Answer: 4.5°E (or 5°E if rounding to 1°)
```

---

### Example 3: Crossing Zero (East to West)

**Find deviation at 188°(C)**

```
Table:
  180° → 0°
  195° → 1°W

Step 1: Bracketing values
  H₁ = 180°, H₂ = 195°
  D₁ = 0°, D₂ = 1°W

Step 2: Position ratio
  P = (188 - 180) ÷ (195 - 180)
  P = 8 ÷ 15 = 0.533

Step 3: Deviation range
  0° = 0
  1°W = -1° (West is negative)
  Range = -1° - 0° = -1°

Step 4: Interpolate
  Deviation = 0° + (0.533 × -1°)
           = -0.533°
           = 0.5°W

Answer: 0.5°W (or 1°W if rounding to 1°)
```

---

### Example 4: West to East Transition

**Find deviation at 338°(C)**

```
Table:
  330° → 2°W
  345° → 2°E

Step 1: Bracketing values
  H₁ = 330°, H₂ = 345°
  D₁ = 2°W, D₂ = 2°E

Step 2: Position ratio
  P = (338 - 330) ÷ (345 - 330)
  P = 8 ÷ 15 = 0.533

Step 3: Deviation range
  2°W = -2°
  2°E = +2°
  Range = (+2°) - (-2°) = +4°

Step 4: Interpolate
  Deviation = -2° + (0.533 × 4°)
           = -2° + 2.13°
           = +0.13°
           = 0.1°E

Answer: 0°E or 0.5°E (essentially zero)
```

---

## Common Interpolation Scenarios

### Scenario A: 15° Table Intervals

**Most Common** – Table entries every 15°

Example: 000°, 015°, 030°, 045°...

**Interpolation frequency:** Often needed
**Precision:** Good (±0.5°)

---

### Scenario B: 30° Table Intervals

**Wider Spacing** – Table entries every 30°

Example: 000°, 030°, 060°, 090°...

**Interpolation frequency:** Nearly always needed
**Precision:** Moderate (±1°)

---

### Scenario C: 10° or Less

**Fine Resolution** – Modern digital tables

**Interpolation frequency:** Rarely needed
**Precision:** High (±0.25°)

---

## Interpolation Shortcuts

### Mental Math Shortcuts

**Halfway between entries?**
```
If P ≈ 0.5, deviation is average of two values

Example: 097.5° between 090° (5°E) and 105° (5°E)
Result: (5 + 5) ÷ 2 = 5°E
```

**One-quarter or three-quarters?**
```
If P ≈ 0.25 or 0.75, use proportional estimation

Example: 082.5° between 075° (5°E) and 090° (5°E)
P = 0.5, so: 5°E (no change when both same)
```

**Very close to table entry?**
```
If difference < 2°, often acceptable to round to nearest

Example: 091° near 090° (5°E)
Use: 5°E without interpolation
```

---

## East/West Sign Handling

### Sign Convention

| Direction | Numeric Value | Symbol |
|-----------|---------------|--------|
| East      | Positive (+)  | E      |
| West      | Negative (-)  | W      |
| Zero      | 0             | 0° or —|

### Calculation Examples

**East to larger East:**
```
2°E to 5°E
+2 to +5 = range of +3
```

**East to smaller East:**
```
5°E to 3°E
+5 to +3 = range of -2
```

**East to West:**
```
2°E to 3°W
+2 to -3 = range of -5
```

**West to East:**
```
3°W to 2°E
-3 to +2 = range of +5
```

---

## Verification Checks

### After Interpolating, Always Check:

**✓ Reasonableness:**
Does the interpolated value fall between the two table values?

**✓ Direction:**
If both table values are East, result should be East
If both are West, result should be West
If crossing zero, result should be near zero

**✓ Magnitude:**
Interpolated value should not exceed either table value
(unless extrapolating, which you shouldn't do)

**✓ Precision:**
Don't claim false precision – 3.7°E should be 4°E in practice

---

## Practice Problems

**Problem 1:** Find deviation at 022°(C)
Table: 015° → 3°E, 030° → 4°E
<details>
<summary>Answer</summary>
P = 7 ÷ 15 = 0.467
Deviation = 3°E + (0.467 × 1°) = 3.5°E
</details>

**Problem 2:** Find deviation at 263°(C)
Table: 255° → 4°W, 270° → 4°W
<details>
<summary>Answer</summary>
Both values same → 4°W (no interpolation needed)
</details>

**Problem 3:** Find deviation at 172°(C)
Table: 165° → 1°E, 180° → 0°
<details>
<summary>Answer</summary>
P = 7 ÷ 15 = 0.467
Range = 0 - (+1) = -1°
Deviation = 1°E + (0.467 × -1°) = 0.5°E
</details>

---

## Summary Formula Card

```
┌─────────────────────────────────────────┐
│   DEVIATION INTERPOLATION FORMULA       │
├─────────────────────────────────────────┤
│                                         │
│  P = (H - H₁) ÷ (H₂ - H₁)              │
│                                         │
│  D = D₁ + (P × (D₂ - D₁))              │
│                                         │
│  Where:                                 │
│    H  = Target heading                  │
│    H₁ = Lower table heading             │
│    H₂ = Upper table heading             │
│    D₁ = Deviation at H₁                 │
│    D₂ = Deviation at H₂                 │
│    P  = Position ratio (0 to 1)         │
│    D  = Interpolated deviation          │
│                                         │
│  Signs: E = +, W = -                    │
└─────────────────────────────────────────┘
```
