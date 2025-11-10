# Sample Test Prompts for clearing-bearing-calculator

## Test 1: Basic NMT Scenario
**Prompt**: "There's a rock at 50°15'N 004°20'W. I'm passing north of it. The lighthouse at Rame Head is at 50°18'N 004°13'W. What clearing bearing should I use?"

**Expected**: Calculate bearing from rock to lighthouse (~030°T), determine NMT rule (safe water to north/left), provide clear rule and monitoring guidance.

## Test 2: Basic NLT Scenario
**Prompt**: "Shoal at 51°00'N 001°30'W. Passing south of it. Reference is Dover Castle at 51°07'N 001°19'W. Give me the clearing bearing."

**Expected**: Calculate bearing from shoal to castle, determine NLT rule (safe water to south/right), provide clear guidance.

## Test 3: Verify Understanding
**Prompt**: "I want to stay west of a hazard. Reference bearing from hazard is 090°T. Is this NMT or NLT?"

**Expected**: Identify that west (left) of 090°T line requires NMT rule. Explain safe zone is 000-089°T.

## Test 4: Harbor Approach
**Prompt**: "Entering harbor with rocks on port side. Using harbor entrance light as reference. How do I set up clearing bearing?"

**Expected**: Ask for positions, calculate bearing, recognize starboard passage requires NLT rule, provide complete setup.

## Test 5: Multiple Hazards
**Prompt**: "Two rocks: one at 50°20'N 004°10'W and another at 50°22'N 004°15'W. Using Start Point lighthouse. I'm passing between them. Help me set clearing bearings."

**Expected**: Calculate two clearing bearings (NMT for southern rock, NLT for northern rock), explain safe corridor between the two limits.
