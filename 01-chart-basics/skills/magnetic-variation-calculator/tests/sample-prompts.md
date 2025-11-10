# Test Prompts: Magnetic Variation Calculator

## Test 1: Basic Calculation (UK Waters)
**Prompt:** "The compass rose shows 5° 30' W in 2015, annual change 9' E. What's the variation in 2025?"

**Expected Output:**
- Years elapsed: 10
- Total change: 90' = 1° 30'
- Rule: West + East = SUBTRACT
- Calculation: 5° 30' W - 1° 30' = 4° 00' W
- Final answer: **4° W**

---

## Test 2: East Variation
**Prompt:** "Variation is 3° 15' E (2010), changing 6' E per year. Calculate for 2025."

**Expected Output:**
- Years elapsed: 15
- Total change: 90' = 1° 30'
- Rule: East + East = ADD
- Calculation: 3° 15' E + 1° 30' = 4° 45' E
- Final answer: **5° E**

---

## Test 3: Westward Movement
**Prompt:** "Chart dated 2018 shows 2° 40' W, annual change 5' W. What should I use in 2025?"

**Expected Output:**
- Years elapsed: 7
- Total change: 35'
- Rule: West + West = ADD
- Calculation: 2° 40' W + 0° 35' = 3° 15' W
- Final answer: **3° W**

---

## Test 4: Large Time Span
**Prompt:** "Old chart from 2000: variation 8° 10' W, annual change 12' E. Is it still usable in 2025?"

**Expected Output:**
- Years elapsed: 25
- Total change: 300' = 5° 00'
- Rule: West + East = SUBTRACT
- Calculation: 8° 10' W - 5° 00' = 3° 10' W
- Final answer: **3° W**
- Note: Significant drift - verify with current chart/almanac

---

## Test 5: Edge Case - Zero Crossing
**Prompt:** "Variation was 0° 30' W (2020), annual change 10' E. What is it now in 2025?"

**Expected Output:**
- Years elapsed: 5
- Total change: 50'
- Rule: West + East = SUBTRACT
- Calculation: 0° 30' W - 0° 50' = -0° 20' = 0° 20' E
- Final answer: **0° E** (crossed the agonic line!)
- Note: Area has transitioned from West to East variation

---

## Test 6: Incomplete Information
**Prompt:** "Calculate variation for current year"

**Expected Output:**
- Skill should ask for:
  - Base year variation (year, degrees, minutes, direction)
  - Annual change rate (minutes, direction)
  - Target year (or confirm current year 2025)

---

## Test 7: Real Chart Data (Solent)
**Prompt:** "Using BA 2450: 2005 variation 3° 42' W, annual change 9' E. Calculate for 2024."

**Expected Output:**
- Years elapsed: 19
- Total change: 171' = 2° 51'
- Calculation: 3° 42' W - 2° 51' = 0° 51' W
- Final answer: **1° W**
- Context: Solent area approaching zero variation

---

## Validation Criteria
✅ Correct years elapsed calculation
✅ Correct total change (with minutes → degrees conversion)
✅ Correct directional rule applied
✅ Correct arithmetic
✅ Rounded to nearest degree
✅ Clear working shown
✅ Practical notes provided
