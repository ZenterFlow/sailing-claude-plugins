## Sample Test Prompts for Computation of Rates Graph

### Test 1: Standard Interpolation
**Prompt**: "Spring rate is 2.8 knots, neap rate is 1.3 knots. The current range at Dover is 5.4m. MHWS is 6.7m, MHWN is 5.3m. Calculate the actual stream rate."

**Expected Response**:
- Position factor calculation showing 5.4m between 5.3m and 6.7m
- Linear interpolation: (5.4 - 5.3) / (6.7 - 5.3) = 0.07
- Rate calculation: 1.3 + (2.8 - 1.3) × 0.07 = 1.4 knots
- Graphical interpretation description
- Answer: 1.4 knots

### Test 2: Mid-Range Calculation
**Prompt**: "The spring rate at diamond K is 3.0 knots and neap is 1.0 knot. Range at reference port is exactly 5.0m, with MHWS 6.0m and MHWN 4.0m. What rate should I use?"

**Expected Response**:
- Recognition that 5.0m is exactly midway between 4.0m and 6.0m
- Position factor = 0.5 (50%)
- Rate = average of spring and neap = (3.0 + 1.0) / 2 = 2.0 knots
- Verification that midpoint range gives midpoint rate
- Answer: 2.0 knots

### Test 3: Near-Neap Conditions
**Prompt**: "Calculate the tidal stream rate. Spring: 2.5 knots, Neap: 0.9 knots. Current range is 3.8m at Plymouth. MHWS = 5.5m, MHWN = 3.6m."

**Expected Response**:
- Note that 3.8m is very close to MHWN (3.6m)
- Position factor: (3.8 - 3.6) / (5.5 - 3.6) = 0.11
- Rate: 0.9 + (2.5 - 0.9) × 0.11 = 1.1 knots
- Comment that result is close to neap as expected
- Answer: 1.1 knots

### Test 4: Near-Spring Conditions
**Prompt**: "I need the rate for diamond M. Spring rate 3.4 knots, neap 1.6 knots. Range today is 6.4m, with MHWS 6.5m and MHWN 4.8m."

**Expected Response**:
- Note that 6.4m is very close to MHWS (6.5m)
- Position factor: (6.4 - 4.8) / (6.5 - 4.8) = 0.94
- Rate: 1.6 + (3.4 - 1.6) × 0.94 = 3.3 knots
- Comment that result is close to spring as expected
- Answer: 3.3 knots

### Test 5: Extrapolation Above Spring
**Prompt**: "Spring rate 2.6 knots, neap 1.2 knots. The range is 7.1m, which exceeds MHWS of 6.3m. MHWN is 4.5m. What rate should I use?"

**Expected Response**:
- Warning that this requires extrapolation beyond spring
- Position factor: (7.1 - 4.5) / (6.3 - 4.5) = 1.44 (>1.0)
- Rate: 1.2 + (2.6 - 1.2) × 1.44 = 3.2 knots
- Safety note about extrapolation uncertainty
- Graphical note about extending line beyond spring point
- Answer: 3.2 knots (with caution)

### Test 6: Extrapolation Below Neap
**Prompt**: "Calculate rate for spring 2.0 knots, neap 0.8 knots. Range is only 2.9m, below MHWN of 3.4m. MHWS is 5.2m."

**Expected Response**:
- Warning that this requires extrapolation below neap
- Position factor: (2.9 - 3.4) / (5.2 - 3.4) = -0.28 (negative)
- Rate: 0.8 + (2.0 - 0.8) × (-0.28) = 0.5 knots
- Safety note about weak tidal streams
- Graphical note about extending line beyond neap point
- Answer: 0.5 knots

### Test 7: Complex Real-World Scenario
**Prompt**: "I'm planning a passage. Tidal diamond shows springs 3.5 knots at 087°T, neaps 1.8 knots at 087°T. I've calculated the range at Dover will be 5.9m at the time I'm transiting. Dover MHWS = 6.7m, MHWN = 5.3m. What tidal stream should I use for my EP?"

**Expected Response**:
- Full computation showing position factor
- Position: (5.9 - 5.3) / (6.7 - 5.3) = 0.43
- Rate: 1.8 + (3.5 - 1.8) × 0.43 = 2.5 knots
- Note that direction (087°T) doesn't change
- Application note for EP plotting
- Answer: 2.5 knots at 087°T

### Validation Criteria
Each response should:
1. Show all calculation steps clearly
2. Calculate position factor correctly
3. Apply linear interpolation formula
4. Round to 0.1 knot precision
5. Provide graphical interpretation description
6. Include relevant safety warnings for extrapolations
7. State the final rate with appropriate precision
8. Verify result is sensible (between spring/neap for normal interpolation)
