# Sample Test Prompts for velocity-triangle-plotter

## Test 1: Basic CTS Triangle
**Prompt**: "Draw velocity triangle for: desired track 000°T, boat speed 6 kts, stream 090°T at 2 kts."

**Expected**: Triangle showing heading into stream (westward correction), clear labels, measurements.

## Test 2: TMG Triangle
**Prompt**: "I steered 045°T at 5 kts for 2 hours. Stream was 135°T at 1.5 kts. Plot the triangle showing my track made good."

**Expected**: Forward-plotting triangle, showing heading → water track → stream → final TMG.

## Test 3: Following Stream
**Prompt**: "Show triangle: track 180°T, boat speed 5 kts, stream 180°T at 2 kts following."

**Expected**: Simple triangle showing stream assists, SOG = 7 kts, vectors aligned.

## Test 4: Opposing Stream
**Prompt**: "Plot triangle: desired 000°T (north), boat speed 4 kts, stream 180°T at 2 kts opposing."

**Expected**: Triangle showing head-on stream opposition, reduced SOG = 2 kts.

## Test 5: Complex with Leeway
**Prompt**: "Velocity triangle with: track 090°T, boat speed 5 kts, stream 180°T at 2 kts, leeway 5° starboard."

**Expected**: Triangle showing heading → leeway → water track → stream → TMG, all vectors labeled.
