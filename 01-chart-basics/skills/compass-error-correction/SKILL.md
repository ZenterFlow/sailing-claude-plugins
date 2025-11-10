---
name: compass-error-correction
description: Convert between True, Magnetic, and Compass bearings using variation and deviation with CADET mnemonic.
license: CC-BY-SA
---

# SKILL: compass-error-correction
**RYA Yachtmaster – True ↔ Magnetic ↔ Compass Conversion (CADET)**

## Purpose
Teach the systematic conversion between True, Magnetic, and Compass bearings using the CADET mnemonic, combining variation and deviation corrections for accurate navigation.

## Activation Triggers
- "Convert 085°T to compass"
- "CADET conversion"
- "True to compass bearing"
- "Compass to true"
- "Apply variation and deviation"
- "340°C with 5°E deviation and 10°W variation"

## Behaviour
1. Identify the conversion direction:
   - **Compass → True** (C→M→T): ADD East corrections
   - **True → Compass** (T→M→C): Reverse the process

2. Gather required information:
   - Starting bearing and type (True/Magnetic/Compass)
   - Variation (from compass rose or magnetic-variation-calculator)
   - Deviation (from ship's deviation table if converting compass)

3. Apply CADET method:
   - **C**ompass bearing
   - **A**dd
   - **E**ast (deviation and variation)
   - **T**o get True bearing

   **Reverse for True → Compass:**
   - Add West, Subtract East

4. Show complete working:
   - Display each step clearly
   - Apply deviation first (if relevant), then variation
   - Handle 360° wrap-around correctly
   - State final bearing with label (T/M/C)

5. Common patterns to teach:
   - **C→M→T**: "Compass Add East = True"
   - **T→M→C**: "True Subtract East = Compass"

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor prompt with CADET details
- `templates/cadet-diagram.md` – visual CADET mnemonic
- `templates/worked-example.md` – step-by-step conversions
- `tests/sample-prompts.md` – validation questions
- `resources/conversion-table.md` – quick reference table

## Example Session

**User:** "Convert 340°C to True. Deviation is 5°E, variation is 10°W"

**Skill:**
```
COMPASS → TRUE CONVERSION (CADET)

Given:
- Compass bearing: 340°(C)
- Deviation: 5°E
- Variation: 10°W

Step 1: Compass → Magnetic (apply deviation)
  Rule: Add East deviation
  340°(C) + 5°E = 345°(M)

Step 2: Magnetic → True (apply variation)
  Rule: Subtract West variation
  345°(M) - 10°W = 335°(T)

✅ FINAL ANSWER: 335°(T)

CADET CHECK: Compass + East corrections = True ✓
```

**User:** "Now convert 085°T to compass, same errors"

**Skill:**
```
TRUE → COMPASS CONVERSION (Reverse CADET)

Given:
- True bearing: 085°(T)
- Variation: 10°W
- Deviation: 5°E

Step 1: True → Magnetic (reverse variation)
  Rule: Add West variation
  085°(T) + 10°W = 095°(M)

Step 2: Magnetic → Compass (reverse deviation)
  Rule: Subtract East deviation
  095°(M) - 5°E = 090°(C)

✅ FINAL ANSWER: 090°(C)

Reverse CADET: True + West - East = Compass ✓
```

## Key Concepts
- **CADET works one way only**: Compass → True (Add East)
- **Reverse carefully**: True → Compass (Add West, Subtract East)
- **Apply in order**: Always Deviation first, then Variation
- **Label every bearing**: (T), (M), or (C) to avoid confusion
- **360° wrap**: 359° + 3° = 002°, not 362°
