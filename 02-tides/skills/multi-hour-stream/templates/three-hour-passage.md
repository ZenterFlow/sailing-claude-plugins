### Three-Hour Passage Integration Example

**Scenario**: Coastal passage from Ramsgate to North Foreland to Dover

#### Given Information
- Departure: Ramsgate 0900 (HW Dover -2)
- Estimated passage time: 3 hours at 5 knots
- Expected arrival: 1200 (HW Dover +1)

**Tidal Stream Data** (from tidal diamond):
- HW-2 (0900): 1.2 knots at 240°T
- HW-1 (1000): 0.8 knots at 230°T
- HW   (1100): 0.3 knots at 220°T
- HW+1 (1200): 1.5 knots at 045°T

Note: Stream turns around HW Dover in this area

#### Step-by-Step Integration

**Step 1: Calculate tidal distances**
```
Hour 1 (0900-1000, HW-2):
  1.2 knots × 1.0 hour = 1.2 NM at 240°T

Hour 2 (1000-1100, HW-1):
  0.8 knots × 1.0 hour = 0.8 NM at 230°T

Hour 3 (1100-1200, HW):
  0.3 knots × 1.0 hour = 0.3 NM at 220°T
```

**Step 2: Mathematical vector integration**

Convert each to N/E components:

Vector 1: 1.2 NM at 240°T
```
North: 1.2 × cos(240°) = 1.2 × (-0.500) = -0.60 NM
East:  1.2 × sin(240°) = 1.2 × (-0.866) = -1.04 NM
```

Vector 2: 0.8 NM at 230°T
```
North: 0.8 × cos(230°) = 0.8 × (-0.643) = -0.51 NM
East:  0.8 × sin(230°) = 0.8 × (-0.766) = -0.61 NM
```

Vector 3: 0.3 NM at 220°T
```
North: 0.3 × cos(220°) = 0.3 × (-0.766) = -0.23 NM
East:  0.3 × sin(220°) = 0.3 × (-0.643) = -0.19 NM
```

**Step 3: Sum components**
```
Total North: -0.60 + (-0.51) + (-0.23) = -1.34 NM (South)
Total East:  -1.04 + (-0.61) + (-0.19) = -1.84 NM (West)
```

**Step 4: Calculate resultant**
```
Distance = √((1.34)² + (1.84)²)
        = √(1.80 + 3.39)
        = √5.19
        = 2.3 NM

Direction = arctan(1.84 / 1.34)
         = arctan(1.373)
         = 53.9°

Since both components are negative (SW quadrant):
True bearing = 180° + 53.9° = 234°T
```

#### Final Answer
**Integrated tidal vector: 2.3 NM at 234°T**

Equivalent rate: 2.3 NM ÷ 3.0 hours = 0.8 knots at 234°T

#### Graphical Interpretation

```
         N
         ↑
         │
         │
W ←──────┼──────→ E
         │
         │    Origin (Start)
         │      │
         │      │  ← Vec 1: 1.2 NM @ 240°T
         │      │╲
         │      │ ╲
         │      │  ╲← Vec 2: 0.8 NM @ 230°T
         │      │   ╲
         │      │    ╲← Vec 3: 0.3 NM @ 220°T
         │      │     ↓
         │      │   (End point)
         │      │
         │      ╲ Resultant
         │       ╲ 2.3 NM @ 234°T
         │        ↘
         ↓
         S
```

#### Application to Passage Planning

**For Course to Steer** (planning before departure):

1. Plot Ramsgate to Dover on chart
2. Measure ground track: e.g., 050°T, 15.0 NM
3. From Ramsgate, plot integrated tide: 2.3 NM at 234°T
4. From tide endpoint, plot to Dover
5. Measure this line = water track = course to steer
6. This is the course through the water you must make

**For EP Calculation** (if no fixes available):

1. From 0900 Ramsgate position (departure fix)
2. Plot water track: course steered × 5 knots × 3 hours = 15 NM
3. From water track endpoint, plot tidal drift: 2.3 NM at 234°T
4. Final point is your EP at 1200
5. Compare with actual arrival position at Dover when you get fix

#### Verification Checks

✓ All three vectors point generally SW (220-240°) → Resultant should point SW ✓
✓ Resultant (2.3 NM) < sum of vectors (2.3 NM) ✓ (slightly less due to spread)
✓ Equivalent rate (0.8 kn) is reasonable for this area ✓
✓ All calculations in True bearings ✓

#### Time Saved
- Without integration: Plot 3 separate vectors on chart (3 × 2 min = 6 min)
- With integration: Plot 1 vector (2 min)
- Plus: Cleaner chart, less clutter, reduced wear

#### Note on Stream Turn
This example shows a stream turn around HW Dover. The flood (SW-going) streams before HW partially oppose the ebb (NE-going) stream after HW. If passage extended to include more HW+1, HW+2, etc., the NE streams would eventually dominate and resultant would shift more easterly.

**Key Learning**: Integration automatically accounts for stream direction changes over time!
