---
name: compass-error-corrector
description: Convert between True, Magnetic, and Compass bearings using CADET mnemonic and applying variation and deviation.
license: CC-BY-SA
---

# SKILL: compass-error-corrector
**RYA Yachtmaster – Compass Error Correction (T ↔ M ↔ C)**

## Purpose
Convert bearings between True (T), Magnetic (M), and Compass (C) using the CADET mnemonic. Apply variation and deviation corrections in correct order and direction.

## Activation Triggers
- "true to magnetic"
- "compass to true"
- "CADET"
- "convert bearing"
- "apply variation"
- "apply deviation"
- "T M C conversion"

## Behaviour
Use CADET mnemonic for conversions:

### CADET: Compass → True
**C**ompass
**A**dd
**D**eviation
**E**ast
**T**rue

**Step 1: Compass → Magnetic**
- Add East deviation
- Subtract West deviation

**Step 2: Magnetic → True**
- Add East variation
- Subtract West variation

### Reverse (True → Compass)
**Step 1: True → Magnetic**
- Subtract East variation
- Add West variation

**Step 2: Magnetic → Compass**
- Subtract East deviation
- Add West deviation

**Memory Aid**: "Error East, Compass Least; Error West, Compass Best"

## Example Output
```
COMPASS ERROR CORRECTION
═══════════════════════════════════════

GIVEN:
Compass bearing: 340°C
Deviation: 5°E (from deviation table at heading ~340°)
Variation: 10°W (from chart for current year)

CONVERSION: COMPASS → TRUE
─────────────────────────────────────

Step 1: Apply Deviation (C → M)
Compass: 340°C
Deviation: 5°E → ADD
Magnetic: 340° + 5° = 345°M

Step 2: Apply Variation (M → T)
Magnetic: 345°M
Variation: 10°W → SUBTRACT
True: 345° - 10° = 335°T

RESULT:
340°C = 335°T

CADET CHECK:
C (340°) + D (5°E) = M (345°) - V (10°W) = T (335°) ✓

═══════════════════════════════════════

REVERSE CONVERSION: TRUE → COMPASS
─────────────────────────────────────

Given: 335°T

Step 1: Apply Variation (T → M)
True: 335°T
Variation: 10°W → ADD (reverse)
Magnetic: 335° + 10° = 345°M

Step 2: Apply Deviation (M → C)
Magnetic: 345°M
Deviation: 5°E → SUBTRACT (reverse)
Compass: 345° - 5° = 340°C

RESULT:
335°T = 340°C ✓
```

## Special Cases
- **360° wrap-around**: 359° + 3° = 002° (not 362°)
- **Multiple sources**: Variation from chart, deviation from vessel's table
- **Hand bearing compass**: No deviation (portable, no fixed location)

## Step-by-Step Conversion Table
| From | To | East | West |
|------|-----|------|------|
| C→M | Add Dev | Subtract Dev |
| M→T | Add Var | Subtract Var |
| T→M | Subtract Var | Add Var |
| M→C | Subtract Dev | Add Dev |

## Common Errors to Avoid
- Applying variation before deviation (wrong order)
- Mixing up add/subtract for east/west
- Forgetting to reverse operations for True → Compass
- Using hand bearing compass deviation (doesn't exist)
- Wrap-around errors near 000°/360°

## Version
v1.0.0 (2025-11-10)
