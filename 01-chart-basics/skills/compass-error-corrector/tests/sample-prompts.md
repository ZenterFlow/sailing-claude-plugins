# Sample Test Prompts

## Test 1: Basic Compass to True
**Prompt**: "Compass bearing 340°C. Deviation 5°E, variation 10°W. What's the true bearing?"
**Expected**: Step 1: 340+5=345°M, Step 2: 345-10=335°T. Show CADET working.

## Test 2: True to Compass
**Prompt**: "I need to steer 090°T. Variation is 8°W, deviation is 3°E. What compass heading?"
**Expected**: Step 1: 090+8=098°M, Step 2: 098-3=095°C. Show reverse CADET.

## Test 3: Wrap-around Case
**Prompt**: "Compass 002°C, deviation 2°W, variation 5°E. Convert to true."
**Expected**: Step 1: 002-2=000°M (or 360°M), Step 2: 000+5=005°T. Handle wrap-around.

## Test 4: Both Errors East
**Prompt**: "True bearing 180°T. Both deviation and variation are 5°E. What's compass bearing?"
**Expected**: Step 1: 180-5=175°M, Step 2: 175-5=170°C. Show full working.

## Test 5: Hand Bearing Compass
**Prompt**: "Hand bearing compass reads 045°. Variation is 7°W. What's the true bearing?"
**Expected**: Only apply variation (no deviation for hand bearing). 045-7=038°T.

## Test 6: Verification Check
**Prompt**: "Verify: if 340°C with dev 5°E and var 10°W equals 335°T, does the reverse work?"
**Expected**: Show True→Compass: 335+10=345°M, 345-5=340°C ✓ Confirmed.
