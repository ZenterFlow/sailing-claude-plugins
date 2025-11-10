### Partial Hour Integration Example

**Scenario**: Short Channel crossing with non-integer duration

#### Given Information
- Passage: Beachy Head to Dieppe
- Boat speed: 6.5 knots
- Distance: 22 NM
- Estimated passage time: 22 ÷ 6.5 = 3.4 hours (3 hours 24 minutes)
- Departure: 1330 (HW Dover +2)
- Arrival: ~1654 (HW Dover +5 partial)

**Tidal Stream Data**:
- HW+2 (1330): 2.8 knots at 070°T
- HW+3 (1430): 3.2 knots at 075°T
- HW+4 (1530): 2.9 knots at 080°T
- HW+5 (1630): 2.3 knots at 085°T (partial hour)

#### Step-by-Step Integration

**Step 1: Break down time periods**
```
Hour 1 (1330-1430, HW+2):
  Full hour: 2.8 knots × 1.0 hour = 2.8 NM at 070°T

Hour 2 (1430-1530, HW+3):
  Full hour: 3.2 knots × 1.0 hour = 3.2 NM at 075°T

Hour 3 (1530-1630, HW+4):
  Full hour: 2.9 knots × 1.0 hour = 2.9 NM at 080°T

Hour 4 (1630-1654, HW+5):
  Partial hour: 24 minutes = 24/60 = 0.4 hours
  2.3 knots × 0.4 hour = 0.92 NM at 085°T
  Round: 0.9 NM at 085°T
```

**Step 2: Convert to components**

Vector 1: 2.8 NM at 070°T
```
North: 2.8 × cos(70°) = 2.8 × 0.342 = 0.96 NM
East:  2.8 × sin(70°) = 2.8 × 0.940 = 2.63 NM
```

Vector 2: 3.2 NM at 075°T
```
North: 3.2 × cos(75°) = 3.2 × 0.259 = 0.83 NM
East:  3.2 × sin(75°) = 3.2 × 0.966 = 3.09 NM
```

Vector 3: 2.9 NM at 080°T
```
North: 2.9 × cos(80°) = 2.9 × 0.174 = 0.50 NM
East:  2.9 × sin(80°) = 2.9 × 0.985 = 2.86 NM
```

Vector 4: 0.9 NM at 085°T (partial)
```
North: 0.9 × cos(85°) = 0.9 × 0.087 = 0.08 NM
East:  0.9 × sin(85°) = 0.9 × 0.996 = 0.90 NM
```

**Step 3: Sum components**
```
Total North: 0.96 + 0.83 + 0.50 + 0.08 = 2.37 NM
Total East:  2.63 + 3.09 + 2.86 + 0.90 = 9.48 NM
```

**Step 4: Calculate resultant**
```
Distance = √((2.37)² + (9.48)²)
        = √(5.62 + 89.87)
        = √95.49
        = 9.8 NM

Direction = arctan(9.48 / 2.37)
         = arctan(4.00)
         = 76.0°

Both components positive (NE quadrant) → 076°T
```

#### Final Answer
**Integrated tidal vector: 9.8 NM at 076°T**

Equivalent rate: 9.8 NM ÷ 3.4 hours = 2.9 knots at 076°T

#### Graphical Interpretation

```
         N
         ↑
         │       Vector 4: 0.9 NM @ 085° (partial)
         │               ↗
         │       Vector 3: 2.9 NM @ 080°
         │           ↗
         │   Vector 2: 3.2 NM @ 075°
         │       ↗
         │ Vector 1: 2.8 NM @ 070°
         ↗
    Origin ────────→ E

Resultant: 9.8 NM @ 076°T
(from origin to end of vector 4)
```

#### Key Points About Partial Hours

**1. Time Calculation**
```
24 minutes = 24 ÷ 60 = 0.40 hours
30 minutes = 30 ÷ 60 = 0.50 hours
36 minutes = 36 ÷ 60 = 0.60 hours
45 minutes = 45 ÷ 60 = 0.75 hours
```

**2. Distance Calculation**
```
Rate × Time Fraction = Distance

2.3 knots × 0.4 hours = 0.92 NM
```

**3. Don't Skip Partial Hours!**
```
Wrong: "It's only 24 minutes, I'll ignore it"
Impact: Missing 0.9 NM of tidal drift = significant position error

Over 3.4 hour passage:
- With partial hour: 9.8 NM drift
- Without partial hour: ~8.9 NM drift
- Error: ~0.9 NM (almost 1 mile!)
```

**4. When to Use Which Hour's Data**
```
1654 is 24 minutes into HW+5 hour
Therefore use HW+5 rate and direction
Time fraction: 24/60 = 0.4

If passage ended at 1645 (45 min into HW+5):
Use HW+5 rate × 0.75 hour
```

#### Alternative: Rounding to Nearest Hour

**Conservative approach** (if unsure of exact timing):

```
Option A: Round UP to 4 full hours
- Use all 4 hours as full hours
- Over-estimates tidal drift slightly
- Safer if timing uncertain

Option B: Round DOWN to 3 full hours
- Ignore HW+5 hour entirely
- Under-estimates tidal drift
- Less safe

Option C: Interpolate (what we did)
- Use partial hour calculation
- Most accurate
- Best for passage planning
```

**Recommendation**: Always include partial hours for accuracy. Round up only if you want conservative estimate for safety.

#### Verification

✓ All vectors point ENE (070-085°) → Resultant should point ENE ✓
✓ Vectors roughly aligned → Resultant near sum: 2.8+3.2+2.9+0.9 = 9.8 ✓
✓ Partial hour included and calculated correctly ✓
✓ Direction (076°) is average of input directions (70-85°) ✓

#### Application Example

**Course to Steer Calculation**:

1. Ground track desired: Beachy Head to Dieppe = 150°T, 22 NM
2. From Beachy Head, plot tidal drift: 9.8 NM at 076°T
3. From tidal drift endpoint, draw to Dieppe
4. Measure water track: e.g., 135°T, 22.2 NM
5. Course to steer (True): 135°T
6. Speed required: 22.2 ÷ 3.4 = 6.5 knots ✓ (matches boat speed)

The strong ENE tidal stream pushes you right, so you must aim left of track (135° vs 150°).

#### Common Partial Hour Errors

**Error 1: Using full hour when shouldn't**
```
Wrong: 24 minutes = 1 hour
Right: 24 minutes = 0.4 hours
```

**Error 2: Wrong fraction**
```
Wrong: 24 minutes = 0.24 hours
Right: 24 minutes = 24/60 = 0.4 hours
```

**Error 3: Rounding too early**
```
Wrong: 0.92 → 1.0 NM (10% error)
Better: 0.92 → 0.9 NM (2% error)
```

**Error 4: Ignoring partial hour entirely**
```
Wrong: "Close enough, skip it"
Impact: ~1 NM position error = unacceptable
```

#### Mental Check: Is Partial Hour Significant?

**Rule of thumb**: If partial hour accounts for >10% of total drift, include it.

```
This example:
Partial hour drift: 0.9 NM
Total drift: 9.8 NM
Percentage: 0.9 / 9.8 = 9.2%

Close to 10% → Definitely include it!
```

**Another way**: If rate > 2 knots and time > 20 minutes, include it.
