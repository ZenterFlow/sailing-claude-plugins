### Standard Interpolation Example

**Scenario**: Channel passage, need accurate tidal stream rate

#### Given Data
- Location: Tidal diamond "K" on Chart 2669
- Reference port: Dover
- Spring rate at diamond K: 2.8 knots at 045°T
- Neap rate at diamond K: 1.3 knots at 045°T
- Current tidal range at Dover: 5.1m
- Dover ranges: MHWS = 6.7m, MHWN = 5.0m

#### Step-by-Step Calculation

**Step 1: Verify data**
```
Range 5.1m is between MHWN (5.0m) and MHWS (6.7m) ✓
Spring rate (2.8) > Neap rate (1.3) ✓
Rates are for the same direction ✓
```

**Step 2: Calculate position factor**
```
Range span = MHWS - MHWN
           = 6.7 - 5.0
           = 1.7m

Position factor = (Actual Range - MHWN) / Range Span
                = (5.1 - 5.0) / 1.7
                = 0.1 / 1.7
                = 0.059
                ≈ 0.06 (or 6% from neap toward spring)
```

**Step 3: Calculate rate span**
```
Rate span = Spring rate - Neap rate
          = 2.8 - 1.3
          = 1.5 knots
```

**Step 4: Calculate interpolated rate**
```
Adjustment = Rate span × Position factor
           = 1.5 × 0.059
           = 0.088 knots

Interpolated rate = Neap rate + Adjustment
                  = 1.3 + 0.088
                  = 1.388 knots
```

**Step 5: Round to standard precision**
```
1.388 knots → 1.4 knots
```

#### Final Answer
**Rate: 1.4 knots at 045°T**

#### Graphical Interpretation
On the computation of rates graph:
1. Find 1.3 on left (blue/neap) axis, mark point
2. Find 2.8 on right (red/spring) axis, mark point
3. Draw straight line connecting these points
4. Locate 5.1m on horizontal (range) axis
5. Draw vertical line to intersect interpolation line
6. Draw horizontal line to rate axis
7. Read approximately 1.4 knots

#### Application
Use **1.4 knots at 045°T** for:
- Plotting EP from last fix
- Calculating course to steer
- Estimating arrival time
- Assessing leeway and drift

#### Verification Check
- Result (1.4) is between neap (1.3) and spring (2.8) ✓
- Result is much closer to neap than spring ✓ (makes sense: only 6% from neap)
- Precision is 0.1 knot ✓
