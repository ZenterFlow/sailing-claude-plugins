---
name: magnetic-variation-calculator
description: Calculate current magnetic variation using chart compass rose data and annual change rates.
license: CC-BY-SA
---

# SKILL: magnetic-variation-calculator
**RYA Yachtmaster – Magnetic Variation Calculation**

## Purpose
Calculate current magnetic variation from chart compass rose data by applying annual change rates to base year values. Essential for converting between true and magnetic bearings.

## Activation Triggers
- "magnetic variation"
- "variation calculation"
- "compass rose"
- "annual change"
- "update variation"
- "var for this year"

## Behaviour
Calculate variation for target year using formula:
**Variation_Target = Variation_Base ± (Rate × Years)**

### Rules for Annual Change
- **West variation + East movement**: SUBTRACT movement (variation decreasing)
- **West variation + West movement**: ADD movement (variation increasing)
- **East variation + West movement**: SUBTRACT movement (variation decreasing)
- **East variation + East movement**: ADD movement (variation increasing)

### Calculation Steps
1. Read base variation from compass rose (year, value, direction)
2. Read annual change rate (value, direction of movement)
3. Calculate years elapsed: Target_Year - Base_Year
4. Calculate total change: Rate × Years
5. Apply change to base variation (add or subtract based on rules)
6. Convert to degrees and minutes if needed
7. Round to nearest degree for practical use

## Example Output
```
MAGNETIC VARIATION CALCULATION
═══════════════════════════════════════

COMPASS ROSE DATA:
Base year: 2005
Variation: 7° 25' W
Annual change: 8' E (moving eastward)

TARGET YEAR: 2007
Years elapsed: 2007 - 2005 = 2 years

CALCULATION:
─────────────────────────────────────
Total change: 8' × 2 = 16'
Direction: West variation with East movement
Action: SUBTRACT (variation decreasing)

7° 25' W - 16' = 7° 09' W

RESULT FOR 2007:
Variation: 7° 09' W (or 7°W for practical use)

EXPLANATION:
The magnetic pole is moving eastward, so western
variation decreases over time. In 2 years, the
variation has reduced by 16 minutes.
```

## Special Cases
- **Zero crossing**: If calculation crosses 0°, change E/W designation
- **Large time spans**: Annual rate may not be constant over decades
- **Rounding**: For plotting, round to nearest degree (±0.5° acceptable)

## Common Errors to Avoid
- Adding when should subtract (most common error)
- Using wrong base year from compass rose
- Forgetting variation direction moves opposite to annual change
- Not converting minutes to decimal when needed

## Version
v1.0.0 (2025-11-10)
