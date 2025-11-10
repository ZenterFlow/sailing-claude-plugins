# Sample Test Prompts

## Test 1: Basic West Variation with East Movement
**Prompt**: "Compass rose shows 2005: 7°25'W with 8'E annual change. What's the variation in 2007?"
**Expected**: Calculate 2 years, subtract 16', result 7°09'W (or 7°W rounded).

## Test 2: East Variation with West Movement
**Prompt**: "Chart dated 2010, variation 3°10'E, annual change 5'W. Calculate for 2015."
**Expected**: Calculate 5 years, subtract 25', result 2°45'E (or 3°E rounded).

## Test 3: Large Time Span
**Prompt**: "Rose says 1998: 10°W, annual change 6'E. What's today's variation?"
**Expected**: Calculate years from 1998 to current year, apply change, warn about potential inaccuracy over long period.

## Test 4: Practical Rounding
**Prompt**: "Variation calculated as 5°47'W. What should I use for plotting?"
**Expected**: Round to 6°W for practical navigation use.

## Test 5: Direction Confusion
**Prompt**: "I have 8°W moving 5'W annually. After 3 years, do I add or subtract?"
**Expected**: ADD (both west, moving away from zero), result 8°15'W.
