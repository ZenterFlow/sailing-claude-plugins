# Quick EP Plotting Guide

## 3-Step EP Plot

```
┌─────────────────────────────────────┐
│  STEP 1: DEAD RECKONING (DR)       │
├─────────────────────────────────────┤
│ From Last Fix:                      │
│ → Plot Course Steered (True)        │
│ → Measure Distance (Speed × Time)   │
│ → Mark DR △ with time               │
└─────────────────────────────────────┘
          ↓
┌─────────────────────────────────────┐
│  STEP 2: APPLY LEEWAY               │
├─────────────────────────────────────┤
│ From Last Fix (same start):         │
│ → Adjust course by leeway angle     │
│   • Starboard tack: ADD leeway      │
│   • Port tack: SUBTRACT leeway      │
│ → Same distance as DR                │
│ → This gives Water Track position   │
└─────────────────────────────────────┘
          ↓
┌─────────────────────────────────────┐
│  STEP 3: APPLY TIDAL STREAM         │
├─────────────────────────────────────┤
│ From Water Track position:          │
│ → Plot Set (stream direction)       │
│ → Measure Drift (stream speed×time) │
│ → Mark EP ▽▽ with time              │
└─────────────────────────────────────┘
```

---

## Quick Reference Card

### Data Needed
- [ ] Last fix position and time
- [ ] Course steered (compass, magnetic, or true)
- [ ] Speed through water
- [ ] Time elapsed (or current time)
- [ ] Leeway estimate (5-10° typical)
- [ ] Tidal stream set and drift

### Conversions
```
True = Compass + Dev + Var
Distance = Speed (kts) × Time (hrs)
Drift = Stream Speed (kts) × Time (hrs)
```

### Leeway Direction
```
Wind on STARBOARD: ADD leeway to course
Wind on PORT: SUBTRACT leeway from course
```

### Symbols
```
Fix:  ⊙  (circle with dot)
DR:   △  (single triangle)
EP:   ▽▽ (double triangle)
```

---

## 1-Minute Drill

**Given**:
- Fix 10:00 at 50°30'N 002°00'W
- Course 090°T, Speed 6 kts
- Now 11:00 (1 hour)
- Leeway 5° starboard (wind from S)
- Stream 045°T at 2 kts

**Plot**:

**DR (10 seconds)**:
→ 090°T for 6 nm from fix
→ △ 11:00 DR

**Leeway (10 seconds)**:
→ 090° + 5° = 095°T for 6 nm from fix
→ Water track position

**Stream (10 seconds)**:
→ 045°T for 2 nm from water track
→ ▽▽ 11:00 EP

**Total**: 30 seconds to plot, label as complete

---

## Simplified EP (when in a hurry)

If you need quick EP and conditions are simple:

### Method 1: DR Only
- Use if no leeway (motoring) and minimal stream
- Just plot course and distance
- Mark as △ DR

### Method 2: Combined Leeway + Stream
- Calculate approximate combined effect
- Apply as single correction to DR
- Less accurate but fast

### Method 3: GPS COG
- Use GPS Course Over Ground if available
- COG already includes leeway + stream
- Plot distance over ground along COG

---

## Common Shortcuts

### Hourly EP
If updating every hour:
- Last hour's EP becomes new "fix"
- Saves re-plotting from original fix
- **Warning**: Errors accumulate - get real fix every 3 hours

### Negligible Factors
Skip if truly negligible:
- Leeway <2° and short distance: skip leeway
- Stream <0.5 kts and short time: skip stream
- Motor vessel in calm: DR = EP

**But**: Always state assumptions in exam!

---

## Exam Speed Tips

### Pre-calculate
- Work out distance first: Speed × Time
- Work out drift first: Stream × Time
- Have leeway estimate ready (from question or assume 5-7°)

### Plot Efficiently
1. Mark fix ⊙
2. Draw single line from fix (water track = course + leeway)
3. Measure distance along that line
4. From endpoint, draw stream vector
5. Mark EP ▽▽

### Check Your Work
- Does EP make sense?
- Moved in roughly right direction?
- Distance reasonable for time/speed?
- If >20 nm in 1 hour at 5 kts: ERROR!

---

## Troubleshooting

### EP seems too far from DR
**Possible causes**:
- Strong tidal stream ✓ (normal)
- Large leeway in light air ✓ (normal)
- Calculation error ✗ (check math)
- Applied stream twice ✗ (common mistake)

### EP seems too close to DR
**Possible causes**:
- Forgot to apply leeway ✗
- Forgot to apply stream ✗
- Used wrong time interval ✗

### Can't remember which way leeway goes
**Quick check**:
- Look downwind
- That's where boat gets pushed
- Leeway is TOWARD downwind direction

### Stream direction confused
**Remember**:
- SET = where stream is GOING (not coming from)
- Like wind convention is opposite direction
- Check chart carefully

---

## Practice Drill

**Quick 5-Minute EP**:
1. Fix: 50°00'N 005°00'W at 09:00
2. Course: 045°T
3. Speed: 5 kts
4. Time: 2 hours
5. Wind from West (leeway 6° to East)
6. Stream: 090°T at 1.5 kts

**Answer**:
- DR: 050°07'N, 004°52'W (10 nm at 045°T)
- Water track: 051°T (045° + 6° leeway), same distance
- EP: Add stream 090°T for 3 nm from water track
- Final EP: ~50°07'N, 004°48'W

---

## Checklist

Before calling EP complete:

- [ ] Started from last fix (not DR)
- [ ] Converted course to true
- [ ] Calculated distance correctly
- [ ] Applied leeway in correct direction
- [ ] Applied stream from water track (not from fix)
- [ ] Marked EP with ▽▽ and time
- [ ] Assessed confidence level
- [ ] Noted when next fix needed

---

## When EP Goes Wrong

**If EP puts you in impossible position** (e.g., on land):
1. Re-check calculations
2. Check leeway direction (most common error)
3. Check stream direction
4. Check time units (hours not minutes)
5. Verify start position

**If EP disagrees with GPS**:
- GPS is probably right
- Check if GPS is COG or heading
- Use as learning opportunity
- Adjust leeway/stream estimates

**If depth doesn't match**:
- EP may be wrong
- Or tidal height wrong
- Or chart datum wrong
- Get new fix immediately!

---

## Bottom Line

**For RYA Exam**:
- Show all three steps (DR, leeway, stream)
- Use correct symbols
- Label with times
- State confidence

**For Real Navigation**:
- Update frequently
- Validate with depth/transits
- Get fix before hazards
- Trust GPS but know how to plot EP manually
