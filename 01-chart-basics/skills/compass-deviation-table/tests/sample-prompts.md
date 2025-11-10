# Test Prompts: Compass Deviation Table Usage

## Test 1: Exact Table Match
**Prompt:** "My compass heading is 090°. What's the deviation? Table shows: 090° → 5°E"

**Expected Output:**
- Recognition: Exact match in table
- No interpolation needed
- Deviation: **5°E**
- Optional: Show C→M conversion: 090° + 5° = 095°(M)

---

## Test 2: Simple Interpolation (East values)
**Prompt:** "Find deviation for compass heading 081°. Table: 067.5° → 2°E, 090° → 4°E"

**Expected Output:**
- Recognition: Between table entries
- Position calculation: (81 - 67.5) ÷ (90 - 67.5) = 0.60
- Range: 4°E - 2°E = 2°
- Interpolation: 2°E + (0.60 × 2°) = 3.2°E
- Rounded: **3°E** or **3.5°E**
- Show full working

---

## Test 3: Interpolation with Equal Values
**Prompt:** "Compass heading 113°. What's the deviation? Table shows: 105° → 5°E, 120° → 5°E"

**Expected Output:**
- Recognition: Both values are the same
- Conclusion: No interpolation needed
- Deviation: **5°E**
- Note: "Deviation constant across this range"

---

## Test 4: Crossing Zero (East to West)
**Prompt:** "Find deviation at 188°(C). Table: 180° → 0°, 195° → 1°W"

**Expected Output:**
- Recognition: Crossing zero point
- Position: (188 - 180) ÷ (195 - 180) = 0.533
- Range handling: 0° to -1° (West) = -1°
- Interpolation: 0° + (0.533 × -1°) = -0.5°
- Result: **0.5°W** or **1°W**
- Note about sign handling

---

## Test 5: Within 1° of Table Entry
**Prompt:** "Compass 091°. Nearest table entry is 090° → 5°E. Do I need to interpolate?"

**Expected Output:**
- Recognition: Within 1° of table value
- Recommendation: Use nearest value (5°E)
- Rationale: "Difference too small to matter"
- Deviation: **5°E**
- Optional interpolation shown for comparison

---

## Test 6: Magnetic to Compass (Reverse Application)
**Prompt:** "I want to steer 120°(M). Deviation table shows 115° → 4°E and 120° → 3.5°E. What compass heading?"

**Expected Output:**
- Recognition: M→C conversion (reverse)
- Estimate: Try compass near 116°
- Find deviation at 116°(C)
- Interpolation: Between 115° (4°E) and 120° (3.5°E)
- Apply reverse rule: 120°(M) - 3.9°E ≈ 116°(C)
- Verify: 116° + 3.9° ≈ 120°(M) ✓
- Final: **Steer 116°(C)**

---

## Test 7: Westerly Deviation
**Prompt:** "Compass heading 258°. Table: 255° → 4°W, 270° → 4°W. Convert to magnetic."

**Expected Output:**
- Recognition: Both values same (4°W)
- No interpolation needed
- Application: Subtract West for C→M
- Calculation: 258° - 4° = 254°(M)
- Result: **254°(M)**

---

## Test 8: Hand-Bearing Compass Question
**Prompt:** "I took a hand-bearing compass reading of 045°. The deviation table shows 045° → 4°E. What's the magnetic bearing?"

**Expected Output:**
- **Critical recognition**: Hand-bearing compass
- Explanation: "Hand-bearing compass has NO deviation"
- Table doesn't apply
- Answer: **045°(M)** (already magnetic)
- Teaching point about why deviation doesn't apply

---

## Test 9: West to East Transition
**Prompt:** "Find deviation at 338°(C). Table: 330° → 2°W, 345° → 2°E"

**Expected Output:**
- Recognition: Crossing from West to East
- Position: (338 - 330) ÷ (345 - 330) = 0.533
- Range: 2°E - 2°W = (+2) - (-2) = 4°
- Interpolation: -2° + (0.533 × 4°) = 0.13°E
- Result: **0°** or **0.5°E** (essentially zero)
- Note about transition zone

---

## Test 10: Multiple Heading Lookup
**Prompt:** "I need deviations for compass headings: 045°, 067°, and 090°. Table: 000° → 2°E, 045° → 4°E, 090° → 5°E"

**Expected Output:**
For each heading:
- **045°**: Exact match → 4°E
- **067°**: Interpolate between 045° (4°E) and 090° (5°E) → 4.5°E
- **090°**: Exact match → 5°E

Table summary format preferred

---

## Test 11: Old Table Warning
**Prompt:** "This deviation table is dated 2019. Is it still valid?"

**Expected Output:**
- Warning: Table is 5+ years old
- Recommendation: Should be verified/re-swung
- Explanation: Deviation changes with:
  - Electrical equipment changes
  - Structural modifications
  - Compass aging
- Safety note: Use with caution, consider professional check

---

## Test 12: Large Deviation Detection
**Prompt:** "Table shows 090° → 12°E. Is this normal?"

**Expected Output:**
- Recognition: Large deviation (>10°)
- Comment: "Unusually large – compass may need adjustment"
- Recommendation: Consider professional compass swing
- Explanation: Typical deviations are 2-8°
- Safety: Large deviations increase navigation errors

---

## Test 13: Full C→M→T Conversion
**Prompt:** "Compass 081°, deviation from table is 3°E (interpolated), variation 5°W. Convert to True."

**Expected Output:**
- Step 1: Compass → Magnetic
  - 081° + 3°E = 084°(M)
- Step 2: Magnetic → True
  - 084° - 5°W = 079°(T)
- Final: **079°(T)**
- Note: Combined deviation and variation

---

## Test 14: Near-360° Wrap-Around
**Prompt:** "Compass 358°, deviation 4°E. Convert to magnetic."

**Expected Output:**
- Calculation: 358° + 4° = 362°
- Wrap-around: 362° - 360° = 002°(M)
- Result: **002°(M)**
- Note: Handle 360° boundary correctly

---

## Test 15: Interpolation Error Detection
**Prompt:** "Student says deviation at 081° is 2.5°E. Table shows 067.5° → 2°E and 090° → 4°E. Is this correct?"

**Expected Output:**
- Check student work
- Correct calculation:
  - Position: 0.60 (60% of the way)
  - Interpolation: 2° + (0.60 × 2°) = 3.2°E
- Student error identified:
  - Used 0.25 instead of 0.60? Or averaged?
- Correct answer: **3°E** or **3.5°E**
- Teaching moment: Show correct method

---

## Validation Criteria

**For skill to pass assessment:**

✅ **Exact Matches**: Correctly identifies when no interpolation needed
✅ **Interpolation Math**: Accurate position and deviation calculations
✅ **East/West Signs**: Proper handling of E/W signs in calculations
✅ **C→M vs M→C**: Correct application direction
✅ **Hand-Bearing Recognition**: Knows deviation doesn't apply
✅ **Wrap-Around**: Handles 360° boundary correctly
✅ **Rounding**: Appropriate precision (0.5° or 1°)
✅ **Safety Notes**: Mentions table currency, large deviations
✅ **Clear Working**: Shows step-by-step calculations
✅ **Labels**: Always includes (C), (M), (T) on bearings

---

## Performance Standards

### Minimum Passing:
- 5/7 correct interpolations
- Correct C→M and M→C application
- Recognition of hand-bearing compass exception

### Proficient:
- 7/7 correct interpolations
- Handles sign changes correctly
- Identifies unusual/large deviations

### Expert:
- All above, plus:
- Solves reverse problems (M→C)
- Combines with variation seamlessly
- Explains common errors clearly
