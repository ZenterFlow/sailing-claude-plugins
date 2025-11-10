## Sample Test Prompts for Multi-Hour Tidal Stream Integration

### Test 1: Simple Three-Hour Integration (Same Direction)
**Prompt**: "Integrate these tidal streams for a 3-hour passage: Hour 1: 2.0 knots at 090°T, Hour 2: 2.5 knots at 095°T, Hour 3: 2.2 knots at 092°T"

**Expected Response**:
- Calculate distance for each hour (2.0 NM, 2.5 NM, 2.2 NM)
- Convert each to N/E components
- Sum components (North ≈ -0.15 NM, East ≈ 6.7 NM)
- Calculate resultant: 6.7 NM at 091°T
- Equivalent rate: 2.2 knots at 091°T
- Note that vectors mostly aligned gives resultant ≈ sum

### Test 2: Two-Hour Passage with Partial Final Hour
**Prompt**: "I need to integrate tides for a 2.5 hour passage. Hour 1: 1.8 kn at 045°T, Hour 2: 2.1 kn at 050°T, Hour 3 (30 minutes): 1.6 kn at 055°T"

**Expected Response**:
- Hour 1: 1.8 × 1.0 = 1.8 NM at 045°T
- Hour 2: 2.1 × 1.0 = 2.1 NM at 050°T
- Hour 3: 1.6 × 0.5 = 0.8 NM at 055°T
- Vector integration calculation
- Resultant: approximately 4.7 NM at 049°T
- Equivalent rate: 1.9 knots at 049°T
- Note partial hour calculation shown

### Test 3: Opposing Streams (Tidal Turn)
**Prompt**: "Passage spans a tidal turn. Hour 1: 2.5 kn at 270°T, Hour 2: 1.8 kn at 265°T, Hour 3: 0.5 kn at 260°T, Hour 4: 1.2 kn at 080°T, Hour 5: 2.0 kn at 085°T. What's the integrated tidal vector?"

**Expected Response**:
- Identify that first 3 hours go west, last 2 go east (opposing)
- Calculate all 5 vectors
- Show component summation with cancellation
- Resultant should show net westerly drift (stronger flood)
- Magnitude less than sum due to opposition
- Comment on cancellation effect
- Approximate result: 3-4 NM at 260-280°T range

### Test 4: Four-Hour Passage Planning
**Prompt**: "Planning a 4-hour crossing. Departure 1000. Tidal streams: HW+1 (1000): 1.5 kn at 135°T, HW+2 (1100): 2.0 kn at 140°T, HW+3 (1200): 2.3 kn at 145°T, HW+4 (1300): 2.5 kn at 150°T. Calculate the resultant tidal vector."

**Expected Response**:
- All four as full hours
- Vectors all SE direction (135-150°)
- Component calculation showing negative North, positive East
- Resultant: approximately 8.3 NM at 143°T
- Equivalent rate: 2.1 knots at 143°T
- Direction is average of input directions
- Application note for course to steer

### Test 5: Short Passage (1.5 Hours)
**Prompt**: "Integrate tides for a 1.5 hour passage. Hour 1: 3.2 kn at 060°T (full hour), Hour 2: 3.5 kn at 065°T (30 minutes)"

**Expected Response**:
- Hour 1: 3.2 NM at 060°T
- Hour 2: 3.5 × 0.5 = 1.75 NM at 065°T (partial)
- Vector integration
- Resultant: approximately 4.9 NM at 061°T
- Equivalent rate: 3.3 knots at 061°T
- Note about handling 30-minute segment

### Test 6: Five-Hour Long Passage
**Prompt**: "Long offshore passage, 5 hours. Tidal streams: 1.2 kn @ 180°T, 1.5 kn @ 185°T, 1.8 kn @ 190°T, 2.0 kn @ 195°T, 1.6 kn @ 200°T (all full hours). Give me the integrated vector."

**Expected Response**:
- Calculate all 5 vectors
- All pointing generally south with slight clockwise curve
- Component summation
- Resultant: approximately 8.0 NM at 191°T
- Equivalent rate: 1.6 knots at 191°T
- Direction matches average of inputs
- Note this saves plotting 5 separate vectors

### Test 7: Real-World Passage Planning Scenario
**Prompt**: "I'm sailing from Beachy Head to Dieppe. Boat speed 6 knots, distance 22 NM, so about 3.7 hours passage time. Departure 0900. Give me the integrated tidal stream for these hours: 0900-1000 (HW-3): 2.8 kn @ 060°T, 1000-1100 (HW-2): 3.1 kn @ 065°T, 1100-1200 (HW-1): 3.3 kn @ 070°T, 1200-1242 (HW, 42 min): 2.9 kn @ 075°T"

**Expected Response**:
- Breakdown showing 3 full hours plus 42-minute partial
- Hour 4 partial: 2.9 × 0.7 = 2.03 NM at 075°T
- Full vector integration with all 4 segments
- Resultant: approximately 11.2 NM at 066°T
- Equivalent rate: 3.0 knots at 066°T
- Application: Strong ENE set requires aiming left of track
- Safety note about cross-channel passage
- Time saved vs hourly plotting

### Validation Criteria
Each response should:
1. Correctly identify full vs partial hours
2. Calculate tidal distances (rate × time) accurately
3. Show vector integration method (mathematical with components)
4. Calculate resultant magnitude and direction correctly
5. Round final results appropriately (0.1 NM, 1°)
6. Express as equivalent rate if useful
7. Provide application guidance (course to steer or EP)
8. Note any special considerations (opposing streams, partial hours)
9. Describe graphical interpretation (tip-to-tail vectors)
10. Include verification checks where appropriate

### Additional Test: Verification Request
**Prompt**: "Check my work: I integrated three 2-knot streams all at 045°T for 3 hours and got 8.5 NM at 045°T. Is this correct?"

**Expected Response**:
- Identify error: should be 6.0 NM, not 8.5 NM
- Explain: 2 kn × 1 hr = 2 NM per hour
- 3 hours × 2 NM = 6 NM total
- All same direction → vectors add directly
- Correct answer: 6.0 NM at 045°T
- Suggest checking calculation steps
