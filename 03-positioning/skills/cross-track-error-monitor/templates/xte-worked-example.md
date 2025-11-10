# XTE Monitoring - Worked Example

## Scenario: Dover Strait TSS Transit

You're transiting Dover Strait northbound TSS lane.

**Passage Plan**:
- Entry point: 50°55'N, 001°20'E
- Track: 045°T (NE through northbound lane)
- Lane width: 1.5 nm
- Planned: Stay on centerline

**Current Status**:
- Position: 51°05'N, 001°35'E
- Time: 1 hour since entry
- Speed: 6 knots

**Question**: Calculate XTE and assess safety.

---

## SOLUTION

### Step 1: Plot Positions

**Entry Point**: 50°55.0'N, 001°20.0'E (marked on chart)

**Current Position**: 51°05.0'N, 001°35.0'E (marked on chart)

**Planned Track**: 045°T line from entry point

### Step 2: Measure Distance Along Track

From entry to point on track at 51°05'N latitude:
- Distance ≈ 11.0 nm along 045°T line

Expected distance in 1 hour at 6 kts: 6 nm
Actual distance traveled: ~11.5 nm

**Initial observation**: Traveled further than expected (stream assist?)

### Step 3: Calculate XTE

**Graphical Method** (on chart):
1. Draw track line 045°T from entry
2. Mark current position 51°05'N, 001°35'E
3. Draw perpendicular from current position to track line
4. Measure perpendicular distance

**Result**: ~0.3 nm to STARBOARD of track

### Step 4: Assess Status

**XTE Assessment**:
```
CROSS-TRACK ERROR: 0.3 nm to STARBOARD
═══════════════════════════════════════

CONTEXT: Dover Strait TSS Northbound Lane
Lane width: 1.5 nm (0.75 nm each side of center)

POSITION ANALYSIS:
─────────────────────────────────────
Centerline: 0.0 nm
Current: +0.3 nm STARBOARD (right of center)
Lane edge: +0.75 nm STARBOARD

Distance to lane edge: 0.75 - 0.3 = 0.45 nm

STATUS: ⚠ WARNING
─────────────────────────────────────
✓ Still within northbound lane
⚠ 40% of lane width used (0.3/0.75)
⚠ Only 0.45 nm from lane boundary
⚠ Drifting toward separation zone
```

### Step 5: Identify Cause

**Analysis**:
- Planned: 045°T for 6 nm (1 hour at 6 kts)
- Actual: 11.5 nm traveled, 0.3 nm starboard error
- **Cause**: Strong NE tidal stream (1.5-2 kts setting NE)

**Stream Effect**:
- Carried further along track (good)
- But also pushed to starboard (bad for lane keeping)

### Step 6: Recommend Correction

**Correction Required**:

**Option A: Return to Centerline**
```
Current position: 0.3 nm starboard
Target: Centerline (0.0 nm)
Distance ahead: 5-10 nm available

Recommended course alteration: 5-7° to PORT
New course: 045° - 6° = 039°T

Monitor XTE every 10 minutes
Expect to regain centerline in 30-45 minutes
```

**Option B: Parallel Track**
```
If traffic prevents altering course:
Maintain 045°T but accept 0.3 nm offset
Monitor closely - do NOT drift further starboard
Be prepared to alter if XTE increases
```

**Chosen Strategy**: Option A (return to centerline)

### Step 7: Implement Correction

**Action**:
1. Alter course to 039°T (6° port correction)
2. Monitor XTE every 10 minutes
3. Check traffic on port side (crossing toward them)
4. Expect gradual return to center over 30-40 minutes

**Expected Result**:
```
Time   XTE          Status
────   ───────────────────────────
Now    0.30 nm stbd  (WARNING)
+10m   0.25 nm stbd  (CAUTION) ✓
+20m   0.15 nm stbd  (CAUTION) ✓
+30m   0.05 nm stbd  (SAFE) ✓
+40m   0.00 nm       (CENTERED) ✓
```

Then return to 045°T to maintain centerline.

### Step 8: Continuing Monitor

**Next Hour Actions**:
- Check XTE every 10-15 minutes
- If XTE grows: increase correction
- If XTE reduces too fast: ease correction
- If XTE stable at center: maintain course

**Log Entry**:
```
1100: 51°05'N 001°35'E, XTE 0.3nm stbd
      Altered to 039°T to regain track
1110: XTE 0.25nm stbd, correction working
1130: XTE 0.05nm stbd, nearly centered
1140: XTE 0.0nm, resumed 045°T
```

---

## KEY LEARNING POINTS

### 1. XTE Must Be Monitored
- Even with GPS, check manually
- Errors accumulate if uncorrected
- Small corrections early >> large corrections late

### 2. TSS Requirements Are Strict
- Must stay within lane boundaries
- 0.3 nm XTE in 1.5 nm lane = 40% of lane used (WARNING level)
- Separation zone crossing = COLREGS violation

### 3. Understand Cause
- NE stream pushed vessel NE (along AND across track)
- Need to adjust course to counter stream
- Correction must account for continuing stream

### 4. Gradual Corrections
- 6° course change to regain over 30 minutes
- Avoids overshooting
- Smoother track for crew and traffic

### 5. Document Everything
- Log XTE checks
- Record course alterations
- Note traffic situation
- Required for MCA/RYA exams and real-world safety

---

## ALTERNATIVE SCENARIOS

### Scenario A: XTE 0.1 nm
```
STATUS: ✓ SAFE (CAUTION)
ACTION: Minor correction (2-3° port)
URGENCY: Low - routine adjustment
```

### Scenario B: XTE 0.5 nm
```
STATUS: ✗ WARNING (near edge)
ACTION: Immediate correction (10° port)
URGENCY: High - approaching lane boundary
CHECK: Traffic, may need to slow/alter significantly
```

### Scenario C: XTE 0.8 nm (OUTSIDE LANE)
```
STATUS: ✗ DANGER (outside lane)
ACTION:
  1. Immediate course to return (15-20° correction)
  2. Reduce speed if traffic conflict
  3. Sound signal if necessary (5 short blasts)
  4. Consider VHF notification to traffic control
  5. Log incident
URGENCY: CRITICAL
```

---

## SUMMARY

**Initial XTE**: 0.3 nm to starboard

**Assessment**: WARNING (within lane but approaching edge)

**Action**: Alter 6° to port (039°T)

**Outcome**: Return to centerline in 30-40 minutes

**Monitoring**: Every 10 minutes until stable

**Lesson**: Monitor XTE continuously, correct early, understand environmental effects
