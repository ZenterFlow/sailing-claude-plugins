# Sample Test Prompts for visual-fix-calculator

## Test 1: Standard Three-Point Fix
**Prompt**:
"I have three compass bearings: Eddystone Lighthouse 032°C, Rame Head 098°C, Penlee Point 155°C. My compass deviation is 4°W and the chart shows variation 5°W. What's my position?"

**Expected Behavior**:
- Convert each bearing: C→M→T
- Calculate reciprocals
- Check bearing geometry (should be good: ~66° and ~57° separation)
- Assess cocked hat quality
- Provide position

**Key Points to Check**:
- Correct application of CADET (both dev and var are West = subtract)
- Reciprocals calculated correctly
- Bearing geometry assessed
- Quality rating given

---

## Test 2: Poor Bearing Geometry
**Prompt**:
"Three bearings: North Point 010°C, East Head 025°C, South Stack 280°C. Deviation 0°, Variation 3°E. Is this a good fix?"

**Expected Behavior**:
- Convert bearings correctly
- Identify poor geometry (010° and 025° only 15° apart - shallow cut)
- Warn about unreliable intersection
- Suggest taking different bearings or waiting for better angle
- Still provide best position but flag it as POOR quality

**Key Points to Check**:
- Warns about shallow cut (<30°)
- Recommends different objects or waiting
- Clear quality warning

---

## Test 3: Two-Bearing Fix Only
**Prompt**:
"I can only see two objects: Anvil Point lighthouse at 045°C and St Albans Head at 135°C. Deviation 2°E, Variation 4°W. Where am I?"

**Expected Behavior**:
- Accept two-bearing fix
- Note 90° separation (ideal for 2-point fix)
- Provide position at intersection
- Note higher uncertainty than 3-point fix
- Suggest adding third bearing when available

**Key Points to Check**:
- Accepts 2-bearing fix
- Notes this is less reliable than 3-point
- 90° separation identified as good

---

## Test 4: Running Fix
**Prompt**:
"At 14:00 I took a bearing to Start Point: 315°C. At 14:30 I took another bearing to the same point: 000°C. I've been steering 090°T at 5 knots. Deviation 3°W, Variation 5°E. What's my position?"

**Expected Behavior**:
- Identify this as a running fix scenario
- Calculate distance run (2.5 nm in 30 minutes at 5 kts)
- Transfer first position line forward
- Intersect with second bearing
- Warn about accumulated errors
- Mark as ACCEPTABLE quality

**Key Points to Check**:
- Recognizes running fix
- Transfers position line correctly
- Calculates distance run
- Warns about lower accuracy
- May mention four-point bearing rule if applicable

---

## Test 5: Cocked Hat Analysis
**Prompt**:
"I plotted three bearings and got a cocked hat about 0.8 nm across. The bearings were: Berry Head 045°T, Ore Stone 120°T, Mew Stone 190°T. What should I do?"

**Expected Behavior**:
- Identify cocked hat as TOO LARGE (>0.5 nm)
- Recommend re-taking bearings immediately
- Check bearing geometry (reasonable spacing: 75° and 70°)
- Since geometry is OK, suggest systematic error:
  - Wrong object identified?
  - Deviation incorrect?
  - Compass issue?
- **DO NOT** accept this fix for navigation
- Clear instruction to re-take bearings

**Key Points to Check**:
- Flags 0.8 nm as unacceptable
- Recommends immediate re-check
- Suggests checking for systematic errors
- Clear safety warning

---

## Test 6: Complex Scenario with Range
**Prompt**:
"Visual fix with: Needles Lighthouse bearing 270°C, range 2.5 nm (from radar). Hurst Point 330°C. St Catherine's Point 175°C. Deviation 1°W, Variation 3°W. Give me a full quality assessment."

**Expected Behavior**:
- Process all three bearings
- Note that range provides additional validation (no compass error on range)
- Position should align with 2.5 nm circle from Needles
- Check if all position lines (including range circle) agree
- Provide comprehensive quality assessment
- Higher confidence due to range data

**Key Points to Check**:
- Uses range as additional validation
- Notes range is more accurate than bearings
- Comprehensive quality assessment
- May weight range more heavily

---

## Performance Criteria

Each test should demonstrate:
1. ✓ Correct bearing conversions (C→M→T)
2. ✓ Correct reciprocal calculations
3. ✓ Bearing geometry assessment
4. ✓ Quality evaluation with clear ratings
5. ✓ Appropriate warnings and recommendations
6. ✓ Step-by-step workings shown
7. ✓ Position given in Lat/Long or grid reference
8. ✓ Teaching points included where relevant
