# SKILL: Multi-Factor Compass Conversion for Course to Steer

## Description
Execute the complete compass correction sequence for CTS: True → Leeway → Variation → Deviation → Compass, applying each factor in the correct order.

## Prerequisites
- SKILL_44 (Leeway for CTS)
- SKILL_21 (Compass Error Correction)
- SKILL_22 (Deviation Tables)

## Learning Objectives
- Apply leeway, variation, and deviation sequentially
- Recalculate deviation after leeway adjustment
- Demonstrate why deviation must be last in sequence
- Handle 360° wrap-around correctly
- Calculate final Compass Course for helmsman

## Conversion Sequence
**Step 1: True Course (from vector triangle)**
- Measure water track bearing = True CTS (pre-leeway)

**Step 2: Apply Leeway**
- Determine wind side (port/subtract, starboard/add)
- **Port wind:** True CTS - leeway = Magnetic Direction (pre-variation)
- **Starboard wind:** True CTS + leeway = Magnetic Direction

**Step 3: Apply Variation**
- Use Mag Var calculation (SKILL_20)
- Add West variation, Subtract East variation
- Result = Magnetic Course (pre-deviation)

**Step 4: Apply Deviation**
- Look up deviation for Magnetic Course in deviation table
- Interpolate if necessary
- Add East deviation, Subtract West deviation (Compass→Magnetic)
- Reverse for Magnetic→Compass: Subtract East, Add West

**Step 5: Final Compass Course**
- Result = Course to Steer for helmsman
- Round to nearest degree

**Why Deviation is Last:**
- Leeway changes vessel heading → changes deviation
- Deviation depends on vessel's magnetic heading
- Must recalculate deviation after leeway applied

**Complete Example:**
- True CTS: 090°(T)
- Port wind, leeway 10° → 080°(T)
- Variation 7°W → 087°(M)
- Deviation: 3°E (for 087°) → 084°(C)
- Compass Course = 084°(C)

## Common Errors
- Wrong order: applying deviation before leeway
- Forgetting to recalculate deviation after leeway
- Wrong deviation application direction (E/W confusion)
- Wrap-around errors (e.g., 357° + 5° = 002°)

## Assessment
- Complete 5 CTS conversions with 100% accuracy
- Identify correct deviation for leeway-adjusted course
- Explain why sequence order matters
- Handle wrap-around cases correctly