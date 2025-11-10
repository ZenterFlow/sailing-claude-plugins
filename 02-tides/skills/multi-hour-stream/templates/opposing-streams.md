### Opposing Tidal Streams Integration Example

**Scenario**: Passage spanning a tidal turn (streams reverse direction)

#### Given Information
- Location: Thames Estuary
- Passage: 5 hours starting 0800
- Boat: 5 knots through water
- HW Sheerness: 1100 (in middle of passage)
- Streams turn around HW

**Tidal Stream Data**:
- HW-3 (0800): 2.5 knots at 250°T (flood, inbound)
- HW-2 (0900): 2.0 knots at 245°T (flood, weakening)
- HW-1 (1000): 0.8 knots at 240°T (flood, very weak)
- HW   (1100): 0.2 knots at 060°T (slack turning to ebb)
- HW+1 (1200): 1.5 knots at 070°T (ebb, outbound)

#### Step-by-Step Integration

**Step 1: Identify opposing streams**
```
Flood (inbound): Hours 1-3, pointing SW (240-250°)
Ebb (outbound): Hours 4-5, pointing NE (060-070°)

These oppose each other → Will partially cancel out
```

**Step 2: Calculate distances**
```
Hour 1 (0800, HW-3): 2.5 × 1.0 = 2.5 NM at 250°T
Hour 2 (0900, HW-2): 2.0 × 1.0 = 2.0 NM at 245°T
Hour 3 (1000, HW-1): 0.8 × 1.0 = 0.8 NM at 240°T
Hour 4 (1100, HW):   0.2 × 1.0 = 0.2 NM at 060°T
Hour 5 (1200, HW+1): 1.5 × 1.0 = 1.5 NM at 070°T
```

**Step 3: Convert to components**

Vector 1: 2.5 NM at 250°T
```
North: 2.5 × cos(250°) = 2.5 × (-0.342) = -0.85 NM
East:  2.5 × sin(250°) = 2.5 × (-0.940) = -2.35 NM
```

Vector 2: 2.0 NM at 245°T
```
North: 2.0 × cos(245°) = 2.0 × (-0.423) = -0.85 NM
East:  2.0 × sin(245°) = 2.0 × (-0.906) = -1.81 NM
```

Vector 3: 0.8 NM at 240°T
```
North: 0.8 × cos(240°) = 0.8 × (-0.500) = -0.40 NM
East:  0.8 × sin(240°) = 0.8 × (-0.866) = -0.69 NM
```

Vector 4: 0.2 NM at 060°T
```
North: 0.2 × cos(60°) = 0.2 × (0.500) = +0.10 NM
East:  0.2 × sin(60°) = 0.2 × (0.866) = +0.17 NM
```

Vector 5: 1.5 NM at 070°T
```
North: 1.5 × cos(70°) = 1.5 × (0.342) = +0.51 NM
East:  1.5 × sin(70°) = 1.5 × (0.940) = +1.41 NM
```

**Step 4: Sum components**
```
North components:
Flood: -0.85 + (-0.85) + (-0.40) = -2.10 NM (south)
Ebb:   +0.10 + 0.51                = +0.61 NM (north)
Total North: -2.10 + 0.61          = -1.49 NM (net south)

East components:
Flood: -2.35 + (-1.81) + (-0.69) = -4.85 NM (west)
Ebb:   +0.17 + 1.41                = +1.58 NM (east)
Total East: -4.85 + 1.58           = -3.27 NM (net west)
```

**Step 5: Calculate resultant**
```
Distance = √((-1.49)² + (-3.27)²)
        = √(2.22 + 10.69)
        = √12.91
        = 3.6 NM

Direction = arctan(3.27 / 1.49)
         = arctan(2.195)
         = 65.5°

Both components negative (SW quadrant):
True bearing = 180° + 65.5° = 246°T
```

#### Final Answer
**Integrated tidal vector: 3.6 NM at 246°T**

Equivalent rate: 3.6 NM ÷ 5.0 hours = 0.7 knots at 246°T

#### Key Observations

**1. Cancellation Effect**
```
Total flood drift: 2.5 + 2.0 + 0.8 = 5.3 NM (if all SW)
Total ebb drift:   0.2 + 1.5       = 1.7 NM (if all NE)

If all same direction: 5.3 + 1.7 = 7.0 NM total
Actual resultant: 3.6 NM

Difference: 7.0 - 3.6 = 3.4 NM canceled out by opposing streams!
```

**2. Dominant Direction**
```
Resultant 246°T is close to flood direction (240-250°T)
This makes sense: flood is stronger than ebb
Flood dominated this passage
```

**3. Importance of Integration**
```
If you only looked at strongest stream (2.5 kn flood):
You'd estimate 2.5 kn set all passage → 12.5 NM drift
Actual drift: 3.6 NM
Error: 8.9 NM! (Huge!)

Integration accounts for stream turn automatically.
```

#### Graphical Interpretation

```
         N
         ↑
         │         Vector 5 (ebb)
         │         ↗
         │   Vector 4 (slack)
         ↗
W ←──────┼──────→ E
         │  ↖
         │    ╲ Vector 3 (flood)
         │     ↘
         │      ╲ Vector 2 (flood)
         │       ↘
         │        ╲ Vector 1 (flood)
         │         ↘
         │          End point
         ↓           ↓
         S           ╲
                      ╲
                       ╲ Resultant
                        ↘ 3.6 NM @ 246°T
                      Origin
```

Notice how vectors "fold back" when stream turns, reducing overall drift.

#### Comparison: Without Integration

**If you plotted each hour separately on chart**:

Hour 1: Drift 2.5 NM SW, plot EP₁
Hour 2: From EP₁, drift 2.0 NM SW, plot EP₂
Hour 3: From EP₂, drift 0.8 NM SW, plot EP₃
Hour 4: From EP₃, drift 0.2 NM NE, plot EP₄
Hour 5: From EP₄, drift 1.5 NM NE, plot EP₅

Result: Same final position, but 5 separate plots on chart
Time: ~10 minutes of plotting
Chart wear: Significant

**With integration**:

Single resultant: 3.6 NM at 246°T from start point
Time: ~2 minutes of plotting
Chart wear: Minimal

#### Application to Passage Planning

**Scenario**: Sailing from A to B, 5-hour passage

**Without considering tidal turn** (wrong method):
```
"Average stream is about 1.4 knots SW"
Drift estimate: 1.4 × 5 = 7 NM SW
WRONG! Ignores ebb streams entirely
```

**With integration** (correct method):
```
Resultant: 3.6 NM at 246°T
This automatically accounts for tidal turn
Much more accurate
```

#### Verification Checks

✓ Flood streams stronger than ebb → Resultant should favor flood direction ✓
✓ Resultant (3.6 NM) < sum of all distances (7.0 NM) ✓ (opposing streams cancel)
✓ Direction (246°T) close to flood average (245°T) ✓
✓ Equivalent rate (0.7 kn) reasonable for net drift ✓

#### Planning Around Tidal Turns

**Strategic timing options**:

**Option A: Departure 0800 (what we calculated)**
- Experience flood for 3 hours
- Then ebb for 2 hours
- Net drift: 3.6 NM SW

**Option B: Departure 1000 (start at slack)**
- Experience minimal flood (1 hour)
- Then ebb for 4 hours
- Net drift would be more easterly

**Option C: Departure 0600 (start at peak flood)**
- Experience flood for 5 hours
- Then slack/turning
- Net drift ~10 NM SW

**Choice depends on**:
- Desired ground track direction
- Available departure windows
- Destination bearing from start point

#### Safety Consideration

**Critical point**: In areas with tidal turns (most coastal waters), you MUST:
1. Check almanac for stream turn time (usually near HW or LW)
2. Calculate streams for before AND after turn
3. Integrate properly to account for opposition
4. Never assume stream is constant direction for multi-hour passage

**Example of danger**:
```
Wrong assumption: "2 knot SW stream all passage"
Reality: Stream turns after 3 hours
Impact:
- Expected position: 10 NM SW of track
- Actual position: 3.6 NM SW of track
- Position error: 6.4 NM!
- Could miss destination, hit hazard, etc.
```

#### Advanced: Optimizing Departure Time

**If you can choose departure time**, integrate for different scenarios:

```
Scenario A (0600 start): Resultant X NM at Y°T
Scenario B (0800 start): Resultant 3.6 NM at 246°T
Scenario C (1000 start): Resultant Z NM at W°T

Pick scenario where resultant most favors your desired ground track.
```

This is why professional passage planning always includes tidal integration!

#### Mental Quick Check

**Opposing streams rule**:
- If passage includes tidal turn
- Streams will partially cancel
- Resultant < sum of magnitudes
- Direction will favor stronger stream

If your calculation doesn't show this, recheck your work!
