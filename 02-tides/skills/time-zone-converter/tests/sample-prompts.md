## Sample Test Prompts for Time Zone Converter

### Test 1: Basic Zone to UT (West)
**Prompt**: "Convert 1530 Zone -1 to UT"

**Expected Response**:
- Show: Zone -1 means UT - 1, so to get UT, add 1 hour
- Calculation: 1530 + 1 hour = 1630 UT
- Answer: 1530 Zone -1 = 1630 UT

### Test 2: Basic UT to Zone (East)
**Prompt**: "Convert 0945 UT to Zone +2"

**Expected Response**:
- Show: Zone +2 = UT + 2 hours
- Calculation: 0945 + 2 hours = 1145 Zone +2
- Answer: 0945 UT = 1145 Zone +2

### Test 3: Zone with DST to UT
**Prompt**: "What is 1620 Zone -1 DST in UT?"

**Expected Response**:
- Step 1: Remove DST → 1520 Zone -1
- Step 2: Convert Zone -1 to UT → 1620 UT
- Show that offsets cancel out
- Answer: 1620 Zone -1 DST = 1620 UT

### Test 4: UT to BST
**Prompt**: "HW Dover is 0842 UT on 15 June. What time is this in BST?"

**Expected Response**:
- State: BST = GMT + 1 = UT + 1 (in summer)
- Calculation: 0842 + 1 hour = 0942 BST
- Answer: HW Dover occurs at 0942 BST
- Safety note: Almanac times are usually in UT

### Test 5: Complex DST Conversion
**Prompt**: "Convert 2130 Zone +3 DST to UT"

**Expected Response**:
- Step 1: Remove DST → 2030 Zone +3
- Step 2: Zone +3 to UT (subtract 3) → 1730 UT
- Total offset: -4 hours
- Answer: 2130 Zone +3 DST = 1730 UT

### Test 6: UT to Zone with DST
**Prompt**: "Convert 1200 UT to Zone -2 DST"

**Expected Response**:
- Step 1: Apply zone → 1200 - 2 = 1000 Zone -2
- Step 2: Add DST → 1000 + 1 = 1100 Zone -2 DST
- Total offset: -1 hour
- Answer: 1200 UT = 1100 Zone -2 DST

### Test 7: Date Line Crossing
**Prompt**: "It's 2245 UT on 23 March. What time and date is it in Zone +12?"

**Expected Response**:
- Calculation: 2245 + 12 hours = 1045 (next day)
- Date changes: crosses into 24 March
- Answer: 2245 UT (23 March) = 1045 Zone +12 (24 March)
- Warning: Date line crossed

### Validation Criteria
Each response should:
1. Show all intermediate steps clearly
2. State the conversion rule being applied
3. Perform arithmetic correctly
4. Use correct 24-hour time format
5. Include relevant warnings (DST status, date line, etc.)
6. Explain the logic, not just give the answer
