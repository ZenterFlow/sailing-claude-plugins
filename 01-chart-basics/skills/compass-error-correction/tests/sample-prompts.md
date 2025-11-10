# Test Prompts: Compass Error Correction

## Test 1: Basic Compass → True
**Prompt:** "Convert 340°C to True. Deviation is 5°E, variation is 10°W."

**Expected Output:**
- Step 1: 340° + 5°E = 345°(M)
- Step 2: 345° - 10°W = 335°(T)
- Answer: **335°(T)**

---

## Test 2: True → Compass
**Prompt:** "I need to steer 085°T on my compass. Variation is 7°W, deviation is 3°E. What compass course?"

**Expected Output:**
- Step 1: 085° + 7°W = 092°(M)
- Step 2: 092° - 3°E = 089°(C)
- Answer: **089°(C)**

---

## Test 3: All East Errors
**Prompt:** "Compass bearing 230°C, deviation 4°E, variation 6°E. Convert to True."

**Expected Output:**
- Step 1: 230° + 4°E = 234°(M)
- Step 2: 234° + 6°E = 240°(T)
- Answer: **240°(T)**

---

## Test 4: All West Errors
**Prompt:** "Convert 180°T to compass. Both deviation and variation are 5°W."

**Expected Output:**
- Step 1: 180° + 5°W = 185°(M)
- Step 2: 185° + 5°W = 190°(C)
- Answer: **190°(C)**

---

## Test 5: Wrap-Around (High Bearing)
**Prompt:** "Compass 358°C, deviation 6°E, variation 2°E. What's the True bearing?"

**Expected Output:**
- Step 1: 358° + 6°E = 364° → 004°(M)
- Step 2: 004° + 2°E = 006°(T)
- Answer: **006°(T)**
- Note: Wrap-around handled correctly

---

## Test 6: Mixed Errors (E and W)
**Prompt:** "Convert 120°C to True. Deviation 4°W, variation 5°E."

**Expected Output:**
- Step 1: 120° - 4°W = 116°(M)
- Step 2: 116° + 5°E = 121°(T)
- Answer: **121°(T)**

---

## Test 7: Magnetic → True Only
**Prompt:** "Magnetic bearing is 270°M. Variation is 8°W. Convert to True."

**Expected Output:**
- Calculation: 270° - 8°W = 262°(T)
- Answer: **262°(T)**
- Note: Single step (no deviation)

---

## Test 8: Zero Deviation
**Prompt:** "True bearing 045°T, no deviation, variation 10°W. What's the compass bearing?"

**Expected Output:**
- Step 1: 045° + 10°W = 055°(M)
- Step 2: No deviation to apply: 055°(C)
- Answer: **055°(C)**

---

## Test 9: CADET Explanation Request
**Prompt:** "Explain the CADET mnemonic"

**Expected Output:**
- Definition: Compass Add East (to get) True
- Direction: Works C→M→T only
- Reverse: True→Compass reverses (Add West, Subtract East)
- Include diagram or visual aid

---

## Test 10: Error Detection
**Prompt:** "Convert 090°C to True. Dev 3°W, Var 5°E. Student answer: 098°T. Is this correct?"

**Expected Output:**
- Correct working: 090° - 3°W = 087°(M), 087° + 5°E = 092°(T)
- Student error identified: Likely added West instead of subtracting
- Correct answer: **092°(T)**
- Teaching point: Review CADET direction rules

---

## Validation Criteria

✅ Correct application order (Deviation before Variation)
✅ Correct East/West logic (Add East C→T, Add West T→C)
✅ 360° wrap-around handled properly
✅ All bearings labeled with (T), (M), or (C)
✅ Clear step-by-step working shown
✅ CADET mnemonic referenced appropriately
✅ Student errors explained constructively
