# Sample Test Prompts for ep-calculator

## Test 1: Standard EP with All Factors
**Prompt**:
"Last fix was at 08:00 at position 50°15'N 003°30'W. I've been steering 135°C at 6 knots, it's now 10:00. Wind is from the Northwest Force 4, I'm on starboard tack close-hauled. Estimate leeway at 7°. Tidal stream is 225°T at 1.8 knots. Deviation is 4°W, variation is 6°W. What's my EP?"

**Expected Behavior**:
- Calculate DR first: Course 135°C - 4° - 6° = 125°T, distance 12 nm
- Apply leeway: Wind from NW, starboard tack, add 7° → Water track 132°T
- Apply stream: 225°T for 3.6 nm (1.8 kts × 2 hrs)
- Provide final EP position with confidence assessment
- Show all three positions: DR △, EP ▽▽

**Key Points to Check**:
- All conversions shown (C→M→T)
- Leeway applied correctly (downwind, starboard side)
- Stream plotted from water track, not DR
- Proper symbols used
- Confidence assessment included

---

## Test 2: Simple DR Only (No Leeway/Stream)
**Prompt**:
"I'm motoring in calm conditions. Last fix at 14:00 was 51°00'N 001°00'W. Course 270°T at 7 knots. What's my DR position at 15:30?"

**Expected Behavior**:
- Recognize this is DR request (not EP)
- Calculate distance: 7 kts × 1.5 hrs = 10.5 nm
- Plot 270°T for 10.5 nm
- Mark as DR △ (not EP)
- Note that DR = EP in this case (no environmental factors)

**Key Points to Check**:
- Correctly identifies as DR scenario
- No leeway applied (motoring, calm)
- No stream applied (not mentioned)
- Uses DR symbol △

---

## Test 3: EP with Leeway Only (No Stream Data)
**Prompt**:
"Fix at 11:00: 50°30'N 002°00'W. Steering 045°T at 5.5 knots. Wind from South, Force 3, sailing close-hauled. Current time 12:30. No tidal stream data available. Calculate my EP."

**Expected Behavior**:
- Ask for or estimate leeway (should suggest 6-8° for Force 3 close-hauled)
- Calculate DR: 045°T for 8.25 nm
- Apply leeway: Wind from S, pushed to N (starboard), add ~7°
- Water track: ~052°T for 8.25 nm
- Note: No stream data, so EP = water track position
- Mark as EP ▽▽ but note limited confidence (no stream data)

**Key Points to Check**:
- Provides leeway estimate when not given
- Applies leeway correctly
- Notes limitation (no stream data)
- Still marks as EP (not DR) since leeway applied
- Recommends getting stream data if possible

---

## Test 4: Port Tack Leeway
**Prompt**:
"Last fix 09:00 at 50°00'N 004°00'W. Course 180°T, speed 6 kts, now 10:00. Wind from East Force 4, port tack, leeway 8°. Stream 045°T at 2 kts. Calculate EP."

**Expected Behavior**:
- DR: 180°T for 6 nm
- Leeway: Wind from E, port tack, pushed to W (port side)
- SUBTRACT leeway: 180° - 8° = 172°T
- Water track: 172°T for 6 nm
- Stream: 045°T for 2 nm from water track
- Final EP with symbols

**Key Points to Check**:
- Correctly subtracts leeway (port tack)
- Clear explanation of leeway direction
- Distinguishes starboard vs port tack application

---

## Test 5: Long Passage EP (Multiple Hours)
**Prompt**:
"Fix at 06:00: 49°30'N 005°00'W. Course 090°T at 5 knots. Time now 11:00 (5 hours). Leeway 5° starboard. Stream 135°T at 1.2 knots. What's my EP and how confident are you?"

**Expected Behavior**:
- Calculate full EP correctly
- DR: 090°T for 25 nm (5 kts × 5 hrs)
- Leeway: 095°T for 25 nm
- Stream: 135°T for 6 nm (1.2 kts × 5 hrs)
- **Confidence: LOW** - fix is 5 hours old
- **WARNING**: EP is degraded, GET NEW FIX IMMEDIATELY
- Recommend fix before entering any hazards

**Key Points to Check**:
- Calculates correctly for long time period
- Flags low confidence (>4 hours old)
- Strong recommendation to get new fix
- Explains error accumulation over time

---

## Test 6: DR vs EP Comparison
**Prompt**:
"Compare DR and EP for this scenario: Fix 10:00 at 50°20'N 003°00'W. Course 270°T, 6 knots, time 12:00. Leeway 6° port side (wind from North). Stream 180°T at 2.5 knots. Show both DR and EP."

**Expected Behavior**:
- Calculate DR: 270°T for 12 nm → mark △
- Calculate EP:
  - Leeway: 270° - 6° = 264°T (wind from N, port tack)
  - Stream: 180°T for 5 nm
- Show both positions on chart
- Explain difference: Set/drift = ~6 nm southward
- Mark DR △ and EP ▽▽ clearly

**Key Points to Check**:
- Shows both DR and EP
- Explains difference between them
- Describes set and drift (difference between DR and EP)
- Educational comparison provided

---

## Test 7: Complex Compass Corrections
**Prompt**:
"Fix 13:00: 51°10'N 001°30'E. Course 315°C at 5.5 kts. Time 15:00. Deviation 3°E, Variation 1°E. Wind SW, starboard tack, leeway 7°. Stream 090°T at 1.5 kts. Calculate EP."

**Expected Behavior**:
- Convert: 315°C + 3°E + 1°E = 319°T
- DR: 319°T for 11 nm (5.5 × 2)
- Leeway: Wind SW (225°), starboard tack, add 7° → 326°T
- Stream: 090°T for 3 nm
- Final EP with all steps shown

**Key Points to Check**:
- Correct application of CADET rule (both E, both added)
- All steps shown clearly
- Leeway direction correct
- Final EP reasonable

---

## Test 8: Zero Leeway Scenario
**Prompt**:
"Motoring course 180°T at 7 knots. Fix at 14:00: 50°00'N 002°00'W. Time 15:30. Stream 270°T at 2 knots. What's my position?"

**Expected Behavior**:
- Recognize motoring = negligible leeway
- DR: 180°T for 10.5 nm
- No leeway correction needed
- Stream: 270°T for 3 nm
- EP = DR + stream only
- Mark as EP ▽▽ (stream applied)

**Key Points to Check**:
- Correctly identifies negligible leeway
- Skips leeway step with explanation
- Still applies stream
- Marks as EP not DR (stream included)

---

## Test 9: Estimate Missing Leeway
**Prompt**:
"Last fix 09:00 at 50°15'N 003°45'W. Course 060°T, speed 5 kts, now 11:00. Wind from West Force 5, beating to windward. Stream 135°T at 1.8 kts. Leeway not measured - please estimate and calculate EP."

**Expected Behavior**:
- Estimate leeway: Force 5, close-hauled, suggest 5-7°
- State assumption clearly
- Calculate EP with estimated leeway
- Apply: 060° + ~6° = 066°T (wind from W, starboard)
- Stream: 135°T for 3.6 nm
- Note moderate confidence due to estimated leeway

**Key Points to Check**:
- Provides reasonable leeway estimate
- States assumption clearly
- Uses conditions (Force 5, beating) to inform estimate
- Notes uncertainty in confidence assessment

---

## Test 10: Validation Check
**Prompt**:
"EP calculated as 50°25'N 002°15'W at 12:00. Charted depth here is 45m, datum is CD. Tide height is 3.2m above CD. Depth sounder shows 47m. Is my EP reliable?"

**Expected Behavior**:
- Calculate expected depth: 45m + 3.2m = 48.2m
- Compare with sounder: 47m
- Difference: 1.2m
- **Assessment: GOOD MATCH** (within error)
- Conclude: EP is likely reliable
- Recommend: Continue monitoring, get visual fix when possible

**Key Points to Check**:
- Performs validation calculation
- Compares charted vs actual depth
- Assesses match quality
- Provides navigation recommendation
- Teaching point: importance of validation

---

## Performance Criteria

Each test should demonstrate:
1. ✓ Correct sequence: DR → Leeway → Stream
2. ✓ Accurate bearing conversions
3. ✓ Correct leeway direction (downwind, stbd/port)
4. ✓ Stream plotted from water track (not from fix)
5. ✓ Proper symbols: ⊙ Fix, △ DR, ▽▽ EP
6. ✓ Time labels on all positions
7. ✓ Distance calculations correct
8. ✓ Confidence assessment appropriate
9. ✓ Recommendations for next fix
10. ✓ Educational content (teaching as calculating)
