---
name: deviation-table-reader
description: Use ship's compass deviation table to find and interpolate deviation values for any heading.
license: CC-BY-SA
---

# SKILL: deviation-table-reader
**RYA Yachtmaster – Deviation Table Usage**

## Purpose
Read and interpolate ship's compass deviation table to find deviation corrections for any heading. Essential for accurate compass to magnetic conversions.

## Activation Triggers
- "deviation table"
- "find deviation"
- "interpolate deviation"
- "compass deviation"
- "deviation for heading"
- "ship's compass error"

## Behaviour
Read deviation from table and interpolate if needed:

### Direct Lookup
- Find heading in table (usually 15° or 30° increments)
- Read deviation value and direction (E or W)
- Apply using CADET rules

### Interpolation
- When heading falls between table values
- Calculate proportional position
- Interpolate deviation value
- Round to nearest degree

### Important Notes
- Deviation is specific to ship's compass location
- Changes with ship's heading (magnetic influence varies)
- Does NOT apply to hand bearing compass (portable)
- Must be updated after major electrical/structural changes

## Example Output
```
DEVIATION TABLE LOOKUP
═══════════════════════════════════════

SHIP'S DEVIATION TABLE:
Heading(M)  Deviation
000°        2°E
045°        4°E
090°        6°E
135°        5°E
180°        3°E
225°        1°E
270°        1°W
315°        0°
360°        2°E

QUERY: Find deviation for heading 081°M

SOLUTION:
─────────────────────────────────────
081° falls between 045° and 090°

Table values:
- 045°M: 4°E
- 090°M: 6°E

Interpolation:
Position: (081 - 045) / (090 - 045)
        = 36 / 45
        = 0.80 (80% of the way)

Deviation range: 6°E - 4°E = 2°
Interpolated: 4° + (0.80 × 2°) = 5.6°

RESULT:
Deviation at 081°M: 6°E (rounded)

USAGE:
To convert 081°M to Compass:
081°M - 6°E = 075°C
(Subtract East when going M→C)
```

## Interpolation Formula
```
Deviation = Dev_Low + [(Heading - Head_Low) / (Head_High - Head_Low)] × (Dev_High - Dev_Low)
```

## Special Cases

### 1. Exact Match
```
Heading: 090°M
Table: 090° = 6°E
Result: 6°E (no interpolation needed)
```

### 2. Near Table Value (±2°)
```
Heading: 092°M
Nearest: 090° = 6°E
Result: 6°E (close enough, no interpolation)
```

### 3. Crossing Zero
```
Between: 315° (0°) and 360° (2°E)
Heading: 340°M
Interpolation: 0° → 1°E (halfway)
Result: 1°E
```

### 4. Direction Change (E to W)
```
Between: 225° (1°E) and 270° (1°W)
Heading: 247°M (halfway)
Special case: 0° deviation (crosses zero)
Result: 0°
```

## Deviation Table Structure
```
Compass Heading | Deviation
----------------|----------
000°(C)         | 3°E
045°(C)         | 5°E
090°(C)         | 7°E
...             | ...

OR

Magnetic Heading | Deviation
-----------------|----------
000°(M)          | 3°E
045°(M)          | 5°E
...              | ...
```

**Critical**: Check if table uses Compass or Magnetic headings!

## Common Errors to Avoid
- Using table backwards (M→C vs C→M)
- Not interpolating when >2° from table value
- Applying deviation to hand bearing compass
- Forgetting deviation changes with heading
- Using old table after structural changes to vessel

## Version
v1.0.0 (2025-11-10)
