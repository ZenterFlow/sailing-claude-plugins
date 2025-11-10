# Sample Test Prompts

## Test 1: Exact Match
**Prompt**: "Ship's head 090°M. Deviation table shows 090° = 6°E. What's the deviation?"
**Expected**: 6°E (no interpolation needed, exact match).

## Test 2: Close to Table Value
**Prompt**: "Heading 092°M. Nearest table value is 090° = 6°E. Do I need to interpolate?"
**Expected**: No, within ±2°. Use 6°E.

## Test 3: Requires Interpolation
**Prompt**: "Heading 081°M. Table shows 045°=4°E and 090°=6°E. What's the deviation?"
**Expected**: Interpolate: 81 is 80% between 045-090. Result: ~6°E.

## Test 4: Direction Change (E to W)
**Prompt**: "Heading 247°M. Table shows 225°=1°E and 270°=1°W. Interpolate."
**Expected**: Halfway point crosses zero. Result: 0° or very close to 0°.

## Test 5: Application (M to C)
**Prompt**: "I want to steer 090°M. Deviation is 6°E. What compass heading?"
**Expected**: Subtract East for M→C: 090-6=084°C.

## Test 6: Hand Bearing Compass
**Prompt**: "I took a hand bearing compass reading of 045°. Should I apply the ship's deviation table?"
**Expected**: NO. Hand bearing compass is portable, no deviation. Only apply variation.

## Test 7: Full Table Lookup and Conversion
**Prompt**: "Show me the full deviation table, then find deviation for 205°M and convert to compass."
**Expected**: Display table, interpolate between 180° and 225°, apply M→C conversion.
