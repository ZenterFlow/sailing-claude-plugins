# Sample Test Prompts for cts-calculator

## Test 1: Standard CTS with Stream and Leeway
**Prompt**: "I want to make good 090°T. Boat speed 6 kts. Stream 180°T at 1.5 kts. Wind from NW, leeway 7° starboard tack. Variation 5°W, deviation 3°W. What course do I steer?"

**Expected**: Full vector calculation, water track ~075°T, heading ~082°T, final CTS accounting for variation/deviation.

## Test 2: No Stream
**Prompt**: "Desired track 045°T, boat speed 5 kts, no tidal stream, leeway 5° port tack, variation 4°W. Calculate CTS."

**Expected**: Simple calculation, only leeway and magnetic corrections, CTS = 045° - 5° - 4° = 036°C (approx).

## Test 3: Strong Beam Stream
**Prompt**: "Track 000°T (north), 5 kts boat speed, stream 090°T at 3 kts, no leeway, variation 2°E. CTS?"

**Expected**: Significant westward correction to counter eastward stream, heading ~320-330°T range, show vector triangle.

## Test 4: Stream Too Strong
**Prompt**: "Desired track 270°T (west), boat speed 4 kts, stream 090°T at 5 kts. Can I make this track?"

**Expected**: Identify stream exceeds boat speed, cannot make westward track, will be set eastward, recommend alternatives (wait for tide/motor).

## Test 5: Following Stream
**Prompt**: "Track 135°T, boat speed 5 kts, stream 135°T at 2 kts, leeway 6° starboard, variation 3°W. What's my CTS and SOG?"

**Expected**: Stream assists, CTS ≈ 135° + leeway - variation, SOG = ~7 kts (boosted by following stream).
