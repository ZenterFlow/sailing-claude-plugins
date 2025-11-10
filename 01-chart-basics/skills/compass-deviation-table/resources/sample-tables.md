# Sample Deviation Tables

This document contains example deviation tables from different vessel types to practice deviation table reading and interpolation.

---

## Table 1: Small Steel Yacht (Well-Adjusted)

**Vessel:** S.Y. Seafarer
**Type:** 12m steel sloop
**Date:** 10 June 2024
**Adjuster:** Maritime Compass Services Ltd
**Location:** Plymouth Sound

```
╔══════════════════╦═══════════════╗
║ COMPASS HEADING  ║   DEVIATION   ║
╠══════════════════╬═══════════════╣
║      000°        ║      2°E      ║
║      015°        ║      3°E      ║
║      030°        ║      4°E      ║
║      045°        ║      4°E      ║
║      060°        ║      5°E      ║
║      075°        ║      5°E      ║
║      090°        ║      5°E      ║
║      105°        ║      5°E      ║
║      120°        ║      4°E      ║
║      135°        ║      3°E      ║
║      150°        ║      2°E      ║
║      165°        ║      1°E      ║
║      180°        ║      0°       ║
║      195°        ║      1°W      ║
║      210°        ║      2°W      ║
║      225°        ║      3°W      ║
║      240°        ║      4°W      ║
║      255°        ║      4°W      ║
║      270°        ║      4°W      ║
║      285°        ║      3°W      ║
║      300°        ║      3°W      ║
║      315°        ║      2°W      ║
║      330°        ║      2°W      ║
║      345°        ║      2°E      ║
╚══════════════════╩═══════════════╝
```

### Characteristics:
- **Maximum deviation**: 5°E
- **Pattern**: Classic symmetrical pattern
- **Zero point**: 180° (due south)
- **Quality**: Well-adjusted (max deviation <6°)

### Practice Questions:

1. Find deviation at 052°(C)
2. Find deviation at 267°(C)
3. Convert 113°(C) to Magnetic
4. To steer 200°(M), what compass heading?

<details>
<summary>Answers</summary>

1. Between 045° (4°E) and 060° (5°E)
   - P = 7/15 = 0.467
   - Dev = 4°E + (0.467 × 1°) = 4.5°E

2. Between 255° (4°W) and 270° (4°W)
   - Both same → 4°W

3. 113°(C), between 105° (5°E) and 120° (4°E)
   - P = 8/15 = 0.533
   - Dev = 5°E + (0.533 × -1°) = 4.5°E
   - 113° + 4.5° = 117.5°(M)

4. Estimate compass ~202°
   - Dev at 202° ≈ 1.5°W
   - 200°(M) + 1.5°W = 201.5°(C) → Steer 202°(C)
</details>

---

## Table 2: Motor Vessel (Higher Deviations)

**Vessel:** M.V. Channel Trader
**Type:** 18m motor cruiser
**Date:** 15 March 2024
**Adjuster:** South Coast Marine Services
**Location:** Southampton

```
╔══════════════════╦═══════════════╗
║ COMPASS HEADING  ║   DEVIATION   ║
╠══════════════════╬═══════════════╣
║      000°        ║      3°W      ║
║      030°        ║      0°       ║
║      060°        ║      6°E      ║
║      090°        ║      9°E      ║
║      120°        ║      8°E      ║
║      150°        ║      4°E      ║
║      180°        ║      1°W      ║
║      210°        ║      5°W      ║
║      240°        ║      8°W      ║
║      270°        ║      9°W      ║
║      300°        ║      7°W      ║
║      330°        ║      4°W      ║
╚══════════════════╩═══════════════╝
```

### Characteristics:
- **Maximum deviation**: 9°E and 9°W
- **Pattern**: Higher deviations (common on motor vessels)
- **Large range**: 30° intervals (more interpolation needed)
- **Note**: Should consider re-adjustment (deviations >8°)

### Practice Questions:

1. Find deviation at 045°(C)
2. Find deviation at 195°(C)
3. Convert 075°(C) to Magnetic
4. Student claims dev at 045° is 3°E. Correct or wrong?

<details>
<summary>Answers</summary>

1. Between 030° (0°) and 060° (6°E)
   - P = 15/30 = 0.5 (halfway)
   - Dev = 0° + (0.5 × 6°) = 3°E

2. Between 180° (1°W) and 210° (5°W)
   - P = 15/30 = 0.5
   - Dev = -1° + (0.5 × -4°) = -3°W = 3°W

3. Between 060° (6°E) and 090° (9°E)
   - P = 15/30 = 0.5
   - Dev = 6°E + (0.5 × 3°) = 7.5°E
   - 075° + 7.5° = 082.5°(M)

4. CORRECT - matches answer #1
</details>

---

## Table 3: Wooden Yacht (Low Deviations)

**Vessel:** S.Y. Traditional
**Type:** 14m wooden cutter
**Date:** 20 August 2024
**Adjuster:** Classic Yacht Services
**Location:** Cowes, Isle of Wight

```
╔══════════════════╦═══════════════╗
║ COMPASS HEADING  ║   DEVIATION   ║
╠══════════════════╬═══════════════╣
║      000°        ║      1°E      ║
║      030°        ║      1°E      ║
║      060°        ║      2°E      ║
║      090°        ║      2°E      ║
║      120°        ║      1°E      ║
║      150°        ║      0°       ║
║      180°        ║      1°W      ║
║      210°        ║      1°W      ║
║      240°        ║      2°W      ║
║      270°        ║      2°W      ║
║      300°        ║      1°W      ║
║      330°        ║      1°E      ║
╚══════════════════╩═══════════════╝
```

### Characteristics:
- **Maximum deviation**: 2°E and 2°W
- **Pattern**: Very low deviations (wooden construction)
- **Quality**: Minimal magnetic interference
- **Note**: Often acceptable to treat as "no deviation" (<2°)

### Practice Questions:

1. Is interpolation really necessary for this table?
2. Find deviation at 105°(C)
3. Practical question: Can you ignore this deviation table?
4. Convert 225°(C) to Magnetic

<details>
<summary>Answers</summary>

1. Debatable - deviations so small that 1° rounding acceptable
   - For exam: still interpolate
   - For practical sailing: nearest value usually fine

2. Between 090° (2°E) and 120° (1°E)
   - P = 15/30 = 0.5
   - Dev = 2°E + (0.5 × -1°) = 1.5°E

3. Technically no - always use the table
   - Practically: 1-2° deviations often within compass reading error
   - Best practice: still apply, especially for passage planning

4. Between 210° (1°W) and 240° (2°W)
   - P = 15/30 = 0.5
   - Dev = 1°W + (0.5 × 1°W) = 1.5°W
   - 225° - 1.5° = 223.5°(M)
</details>

---

## Comparison Summary

| Vessel Type | Max Dev | Pattern | Cause |
|-------------|---------|---------|-------|
| **Steel Yacht** | 5° | Moderate, symmetrical | Steel hull |
| **Motor Vessel** | 9° | High, asymmetrical | Engine, electronics |
| **Wooden Yacht** | 2° | Low, minimal | Non-ferrous construction |

---

## Common Patterns Explained

### Pattern 1: Maximum East on Easterly Headings
Most vessels show maximum East deviation when heading East (060° to 120°)
- Cause: Vessel's own magnetic field aligned with Earth's field

### Pattern 2: Maximum West on Westerly Headings
Maximum West deviation when heading West (240° to 300°)
- Cause: Vessel's field opposing Earth's field

### Pattern 3: Zero Crossing Points
Most tables cross zero somewhere around North-South axis
- Typically: 180° (south) or 360°/000° (north)

### Pattern 4: Symmetry
Well-adjusted compasses show rough symmetry:
- E/W deviations mirror each other
- Smooth transitions (no sudden jumps)

---

## Table Validity Checklist

Use this checklist to assess if a deviation table is trustworthy:

**✅ VALID if:**
- [ ] Dated within last 2 years
- [ ] Signed by qualified compass adjuster
- [ ] Maximum deviation <8° (well-adjusted)
- [ ] Smooth pattern (no sudden jumps >2° between entries)
- [ ] Logical zero crossing point

**⚠️ CAUTION if:**
- [ ] 2-5 years old (verify if possible)
- [ ] Maximum deviation 8-12° (functional but consider adjustment)
- [ ] Some irregular values (may need spot checks)

**❌ REJECT/RE-SWING if:**
- [ ] Over 5 years old
- [ ] No adjuster signature
- [ ] Maximum deviation >12°
- [ ] Irregular pattern (suggests poor adjustment)
- [ ] Major vessel modifications since date
- [ ] New electrical equipment installed

---

## Practice Exercise Set

Using all three tables above, complete these challenges:

### Exercise A: Multi-Table Comparison
For compass heading 075°:
1. Find deviation on Steel Yacht
2. Find deviation on Motor Vessel
3. Find deviation on Wooden Yacht
4. Convert 075°(C) to Magnetic for each vessel

### Exercise B: Reverse Conversions
You want to steer 120°(M) on each vessel:
1. What compass heading on Steel Yacht?
2. What compass heading on Motor Vessel?
3. What compass heading on Wooden Yacht?

### Exercise C: Error Detection
A student claims:
- "Deviation at 195° on Motor Vessel is 2°W"

Is this correct? If not, what's the error?

### Exercise D: Real-World Scenario
You're delivering the Motor Vessel from Southampton to Cherbourg.
- Course to steer (True): 150°T
- Variation: 2°W
- What compass heading to steer?

<details>
<summary>Exercise Answers</summary>

**Exercise A:**
1. Steel: 5°E → 075° + 5° = 080°(M)
2. Motor: 7.5°E → 075° + 7.5° = 082.5°(M)
3. Wooden: 2°E → 075° + 2° = 077°(M)

**Exercise B:**
1. Steel: ~116°(C)
2. Motor: ~112°(C)
3. Wooden: ~119°(C)

**Exercise C:**
WRONG - should be 3°W (see Table 2, Question 2)

**Exercise D:**
1. True 150° + 2°W = 152°(M)
2. Deviation at ~152°(C) ≈ 4°E (interpolate between 150° and 180°)
3. 152°(M) - 4°E = 148°(C)
4. **Steer 148°(C)**
</details>

---

## Advanced Topic: Deviation Curves

For advanced students, deviation tables can be plotted as curves:

```
Deviation
   +10°|
    +8°|        .----.
    +6°|     .--      --.
    +4°|   .-            -.
    +2°| .-                -.
     0°|.                    .
    -2°|                      .
    -4°|                       .
    -6°|                      .-
    -8°|                   .--
   -10°|________________.--_____
       0°  90°  180°  270°  360°
           Compass Heading
```

This visualization helps identify:
- Maximum deviation points
- Zero-crossing locations
- Asymmetry or irregularities
- Need for re-adjustment

**Teaching Point:** Modern electronic systems may auto-compensate, but understanding manual deviation tables remains essential for:
- Backup navigation
- Exam requirements
- Understanding compass behavior
- Cross-checking electronic systems
