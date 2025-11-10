# Sample Test Prompts

## Test 1: Basic Position Fix
**Prompt**: "I took bearings: Lighthouse 045°M, Headland 315°M, Tower 072°M. Variation 3°W. Plot my position."
**Expected**: Convert each to true (subtract 3°W), plot from objects seaward, show intersection as fix.

## Test 2: Deviation Question
**Prompt**: "I have hand bearing compass reading 045°M. Ship's deviation table shows 5°E at this heading. Should I apply it?"
**Expected**: NO. Hand bearing compass is portable, no deviation. Only apply variation.

## Test 3: Collision Avoidance
**Prompt**: "Vessel bearing at 14:00: 320°M, range 2nm. At 14:05: 320°M, range 1.5nm. What's happening?"
**Expected**: Steady bearing, decreasing range = COLLISION RISK. Alter course substantially and early.

## Test 4: Magnetic Interference
**Prompt**: "I'm taking bearings standing next to the engine. Is this OK?"
**Expected**: NO. Engine is strong magnetic source. Move to bow or stern, 1-2m from metal.

## Test 5: Object Selection
**Prompt**: "I want to fix my position. I can see a lighthouse, small buoy, and tower. Which should I use?"
**Expected**: Lighthouse and tower (charted, conspicuous). Avoid small buoy (hard to identify, less accurate).

## Test 6: Cocked Hat Assessment
**Prompt**: "My three bearings create a triangle about 300m across. Is this good?"
**Expected**: Acceptable for coastal navigation. Check: magnetic interference? bearing geometry? time gap?

## Test 7: Bearing Geometry
**Prompt**: "I took bearings of three objects all within 20° of each other. Why is my fix poor?"
**Expected**: Poor geometry (narrow spread). Need ~60-90° spread for good intersection angles.

## Test 8: Full Fix with Timing
**Prompt**: "Show me how to take a proper 3-point fix from start to finish."
**Expected**:
1. Select 3 objects ~60° apart
2. Take bearings quickly (<2 min)
3. Apply variation only
4. Plot from objects seaward
5. Assess cocked hat size
6. Mark position on chart
