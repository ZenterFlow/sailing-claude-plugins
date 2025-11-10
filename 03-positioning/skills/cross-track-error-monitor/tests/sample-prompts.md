# Sample Test Prompts for cross-track-error-monitor

## Test 1: TSS Navigation
**Prompt**:
"I'm in the Dover Strait northbound TSS. Planned track is 045°T from 51°00'N 001°25'E. Current position is 51°08'N 001°38'E. Calculate my XTE and tell me if I'm safe."

**Expected**: Calculate XTE (~0.2-0.3nm starboard), assess against TSS lane width, provide safety status and recommendations.

---

## Test 2: Coastal Passage
**Prompt**:
"Sailing from Plymouth to Fowey, planned track 095°T. Started at 50°20'N 004°10'W, now at 50°18'N 003°55'W. What's my XTE?"

**Expected**: Calculate XTE (~2nm to port), assess as acceptable for coastal navigation, suggest gentle correction.

---

## Test 3: Channel Navigation
**Prompt**:
"In marked channel, centerline track 180°T. Current position 0.15nm west of centerline. Channel width is 0.4nm total. Am I OK?"

**Expected**: XTE 0.15nm port, only 0.05nm from channel edge, WARNING status, immediate correction needed.

---

## Test 4: Perfect Tracking
**Prompt**:
"Track 270°T from 50°30'N 002°00'W. Now at 50°30'N 001°40'W after 2 hours. What's my XTE?"

**Expected**: Recognize XTE = 0 (same latitude, moved due west), praise good tracking, remind to maintain course.

---

## Test 5: Correction Advice
**Prompt**:
"XTE is 0.4nm starboard in a 2nm wide TSS lane. I'm steering 045°T. What course should I steer to get back on track?"

**Expected**: Recommend 5-10° port correction (038-040°T), monitor for 20-30 mins, gradual return to centerline.
