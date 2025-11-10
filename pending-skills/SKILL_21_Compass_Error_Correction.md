# SKILL: Compass Error Correction (Variation & Deviation)

## Description
Convert between True, Magnetic, and Compass bearings using variation and deviation corrections.

## Prerequisites
- Magnetic variation calculation (SKILL_20)
- Deviation table usage (SKILL_22)

## Learning Objectives
- Apply CADET mnemonic correctly
- Convert T↔M↔C in both directions
- Combine variation and deviation sequentially
- Handle 360° wrap-around calculations

## CADET Mnemonic
**C**ompass bearing
**A**dd
**E**ast
**T**o get True bearing

**Reverse for True to Compass:**
- True to Magnetic: Add West, Subtract East
- Magnetic to True: Subtract West, Add East

**Compass to True (Full Conversion):**
1. Compass → Magnetic: Apply deviation
2. Magnetic → True: Apply variation

**Example:**
- Compass: 340°(C)
- Deviation: 5°E (from table)
- Variation: 10°W
- Step 1: 340° + 5°E = 345°(M)
- Step 2: 345° - 10°W = 335°(T)

## Common Errors
- Applying variation in wrong direction
- Forgetting to apply deviation before variation
- Wrap-around errors (e.g., 359° + 3° = 002°)
- Mixing up east/west application

## Assessment
- Convert 10 bearings T↔M↔C with 100% accuracy
- Complete within 2 minutes per conversion
- Demonstrate interpolation for deviation between table values