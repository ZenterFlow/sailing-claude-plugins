# EP vs DR: What's the Difference?

## Definitions

### Dead Reckoning (DR)
**"What your instruments think you've done"**

- **Course**: Compass heading (converted to true)
- **Distance**: Speed through water × Time
- **No environmental factors** included

**DR Position** = Last Fix + Course Steered + Distance Run

**Symbol**: △ (single triangle)

### Estimated Position (EP)
**"Where you actually are (probably)"**

- **Starts with DR**
- **Plus Leeway**: Sideways drift from wind
- **Plus Tidal Stream**: Water movement
- **Plus any other known factors**

**EP Position** = DR + Leeway + Tidal Stream

**Symbol**: ▽▽ (double triangle)

## Visual Comparison

```
START FIX (09:00)
    ⊙ 50°30'N 002°00'W
    │
    │ Course Steered: 090°T
    │ Speed: 5 kts
    │ Time: 2 hours
    │ Distance: 10 nm
    ▼
DR POSITION (11:00 DR)
    △ 50°30'N 001°40'W  ← Instruments say you're here
    │
    │ Apply Leeway: 5° (wind from S)
    │ Wind pushes to starboard
    ▼
WATER TRACK POSITION
    (intermediate)
    │
    │ Apply Tidal Stream: 135°T, 1.5 kts
    │ Stream set SE, drift 3 nm
    ▼
EP POSITION (11:00 EP)
    ▽▽ 50°27'N 001°38'W  ← Actually probably here
```

## When to Use Each

### Use DR When:
1. **Quick reference** to instruments
2. **Motor vessel** with negligible leeway
3. **Short time periods** (<30 mins)
4. **Calm conditions** (no wind, no stream)
5. **Comparing** with EP to assess set/drift

### Use EP When:
1. **Sailing** (leeway present)
2. **Tidal waters** (stream present)
3. **Navigation planning**
4. **Longer passages** (>30 mins)
5. **Pre-calculating positions** before entry
6. **Most real-world navigation**

## Why Both Matter

### DR Helps Identify Errors
- If DR ≠ EP, you can see effect of wind/stream
- Useful for understanding local conditions
- Helps calibrate leeway estimates

### EP is Reality
- EP is where you actually are (within error)
- Use EP for all navigation decisions
- Plot EP on chart, not DR

### Example Scenario
```
Fix at 10:00: 50°30'N 002°00'W
Course: 090°T, Speed: 6 kts
Time: 1 hour elapsed

DR at 11:00: 50°30'N 001°50'W  (6 nm east)
EP at 11:00: 50°28'N 001°48'W  (2 nm SE of DR)

Difference: Stream set you 2 nm SE
→ Useful to know for future planning!
```

## Symbol Summary

| Type | Symbol | Meaning | Includes |
|------|--------|---------|----------|
| **Fix** | ⊙ | Known position | Visual bearings, GPS |
| **DR** | △ | Instruments only | Course + Speed |
| **EP** | ▽▽ | Best estimate | DR + Leeway + Stream |

## Accuracy Comparison

### Fix
- **Accuracy**: ±0.1-0.5 nm (if good bearings)
- **Confidence**: HIGH
- **Symbol**: Circle ⊙
- **Source**: Visual, radar, GPS

### DR
- **Accuracy**: ±0.5-1 nm per hour
- **Confidence**: MEDIUM (short term only)
- **Symbol**: Single triangle △
- **Errors**: Heading ±5°, speed ±10%

### EP
- **Accuracy**: ±0.3-1 nm per hour
- **Confidence**: MEDIUM (better than DR)
- **Symbol**: Double triangle ▽▽
- **Errors**: DR errors + leeway ±2° + stream ±20%

## Degradation Over Time

| Time Since Fix | DR Accuracy | EP Accuracy |
|----------------|-------------|-------------|
| 0 hours (Fix) | ±0 nm ✓ | ±0 nm ✓ |
| 1 hour | ±0.5 nm | ±0.3 nm ✓ Better |
| 2 hours | ±1.0 nm | ±0.6 nm ✓ Better |
| 3 hours | ±1.5 nm | ±1.0 nm ⚠ Get fix soon |
| 4 hours | ±2.0 nm | ±1.5 nm ⚠ Get fix NOW |
| >4 hours | ±3+ nm ✗ | ±2+ nm ✗ Unreliable |

**Key Point**: EP is always better than DR for actual position, but both degrade with time.

## Worked Example

### Scenario
- **Last Fix**: 08:00 at 50°00'N 005°00'W
- **Course Steered**: 045°T
- **Speed**: 5 knots
- **Current Time**: 10:00 (2 hours elapsed)
- **Wind**: From West (leeway 7° to starboard)
- **Tidal Stream**: 090°T at 2 knots

### DR Calculation (10:00 DR)
```
Distance = 5 kts × 2 hrs = 10 nm
Direction = 045°T (course steered)
DR Position = 50°07'N, 004°52'W
△ 10:00 DR
```

### EP Calculation (10:00 EP)
```
Step 1: Start with DR (above)

Step 2: Apply Leeway
- Wind from W → Leeway to E (starboard)
- Leeway 7° starboard
- Water track = 045° + 7° = 052°T
- Distance still 10 nm
- Position: 50°07.2'N, 004°51.5'W

Step 3: Apply Tidal Stream
- Set: 090°T
- Drift: 2 kts × 2 hrs = 4 nm
- Plot 4 nm at 090°T from water track position

EP Position = 50°07'N, 004°47'W
▽▽ 10:00 EP
```

### Result
- **DR** says: 50°07'N, 004°52'W
- **EP** says: 50°07'N, 004°47'W
- **Difference**: 5 nm eastward
- **Reason**: Strong eastward tidal stream (2 kts for 2 hours = 4 nm east, plus 1 nm from leeway)

**Which to use for navigation?** → **EP** (50°07'N, 004°47'W)

## GPS vs Traditional EP

### GPS Course Over Ground (COG)
- **Already includes** leeway and stream
- COG is like an automated EP
- Use GPS COG for modern navigation
- Still useful to plot traditional EP as backup

### Traditional EP Purpose
1. **Backup** when GPS fails
2. **Training** to understand vectors
3. **Passage planning** (pre-calculate positions)
4. **Understanding** local conditions
5. **Exam requirement** (RYA, ASA, MCA)

## RYA Exam Expectations

### You Must Know:
✓ Difference between DR and EP
✓ When to use each
✓ How to plot both on chart
✓ Correct symbols (△ for DR, ▽▽ for EP)
✓ Calculate EP with leeway and stream

### Common Exam Questions:
1. "Plot DR and EP for this scenario"
2. "What is the set and drift between DR and EP?"
3. "Why is EP different from DR?"
4. "When would you use DR instead of EP?"

### Typical Answer Format:
```
DR 11:00 △ 50°30'N 002°00'W
(Course 090°T, 6 nm)

EP 11:00 ▽▽ 50°28'N 001°58'W
(Leeway 5° stbd, Stream 180°T 2 kts)

Set/Drift: 165°T, 2.5 nm (difference between DR and EP)
```

## Summary

| | DR | EP |
|---|----|----|
| **Meaning** | Dead Reckoning | Estimated Position |
| **Includes** | Course + Speed | DR + Leeway + Stream |
| **Symbol** | △ | ▽▽ |
| **Use** | Reference/comparison | Actual navigation |
| **Accuracy** | ±0.5-1 nm/hr | ±0.3-1 nm/hr |
| **When** | Short term, calm | Always (sailing/tidal) |

**Bottom Line**:
- DR = what instruments show
- EP = where you actually are
- Always navigate using EP (or fix)
