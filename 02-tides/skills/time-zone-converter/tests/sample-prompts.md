# Sample Test Prompts

## Test 1: Basic UT to Zone
**Prompt**: "Convert 1430 UT to Zone -1 (no DST)."
**Expected**: 1430 - 1 = 1330 Zone -1. Show step-by-step.

## Test 2: Zone to UT
**Prompt**: "Convert 0815 Zone +8 to UT."
**Expected**: 0815 - 8 = 0015 UT. Note potential date change.

## Test 3: DST Application
**Prompt**: "Convert 1430 UT to Zone -1 DST (summer time)."
**Expected**: Step 1: 1430-1=1330 Zone -1, Step 2: 1330+1=1430 Zone -1 DST. Result matches UT!

## Test 4: DST to UT
**Prompt**: "Convert 1545 Zone -1 DST to UT."
**Expected**: Remove DST: 1545-1=1445 Zone -1. Convert: 1445+1=1545 UT.

## Test 5: Complex Multi-Zone
**Prompt**: "Convert 0815 Zone +8 to Zone -5 DST."
**Expected**:
- Step 1: 0815 Zone +8 → 0015 UT
- Step 2: 0015 UT → 1915 Zone -5 (previous day)
- Step 3: Add DST → 2015 Zone -5 DST

## Test 6: Tide Prediction Application
**Prompt**: "Almanac shows HW 1124 UT. What time is HW in Zone -1 DST?"
**Expected**: 1124 UT → 1024 Zone -1 → 1124 Zone -1 DST. Same as UT in summer!

## Test 7: Midnight Crossing
**Prompt**: "Convert 0130 Zone +10 on 15th June to UT. What's the date in UT?"
**Expected**: 0130 - 10 = 1530 UT on 14th June. Date changed!

## Test 8: Student Error Correction
**Prompt**: "Student says '1200 Zone -1 = 1100 UT'. Correct them."
**Expected**: WRONG direction! Zone -1 to UT: ADD 1 hour. 1200 Zone -1 = 1300 UT.
