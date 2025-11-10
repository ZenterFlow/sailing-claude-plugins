### Computation of Rates Graph - Visual Guide

#### Graph Structure

```
                    COMPUTATION OF RATES GRAPH

Neap                                                Spring
Rate                                                 Rate
(kn)                                                 (kn)

3.0┤•                                           •    3.0
   │  ╲                                       ╱
2.5┤    ╲                                   ╱      2.5
   │      ╲                               ╱
2.0┤        ╲                           ╱          2.0
   │          ╲                       ╱
1.5┤            ╲                   ╱              1.5
   │              ╲               ╱
1.0┤                ╲           ╱                  1.0
   │                  ╲       ╱
0.5┤                    ╲   ╱                      0.5
   │                      X
0.0┼───────┬───────┬───────┬───────┬───────┬───  0.0
        MHWN      4.0     5.0     6.0    MHWS
              Tidal Range (metres)

Legend:
• = Plotted points (neap left, spring right)
╲╱ = Interpolation line
X = Example reading point
```

#### Example 1: Standard Interpolation

**Given**:
- Neap rate: 1.2 knots (plot on LEFT axis)
- Spring rate: 2.8 knots (plot on RIGHT axis)
- Actual range: 5.1m
- MHWN: 4.2m, MHWS: 6.3m

**Plotting Steps**:

1. **Find neap point**: Locate 1.2 on left vertical axis, mark a point
2. **Find spring point**: Locate 2.8 on right vertical axis, mark a point
3. **Draw line**: Connect the two points with a straight line (use ruler)
4. **Find range**: Locate 5.1m on horizontal axis
5. **Read vertically**: Draw vertical line up from 5.1m to intersect your line
6. **Read horizontally**: From intersection, read left to rate axis
7. **Result**: Approximately 2.0 knots

```
Neap                                              Spring
Rate                                               Rate
2.8┤                                           •    2.8
   │                                         ╱
2.4┤                                       ╱      2.4
   │                                     ╱
2.0┤                              [X]  ╱          2.0
   │                                ⎜╱
1.6┤                                ⎟              1.6
   │                              ╱⎟
1.2┤•                           ╱  ⎟              1.2
   │                         ╱    ⎟
0.8┤                       ╱      ⎟              0.8
   │                     ╱        ⎟
0.4┤                   ╱          ⎟              0.4
   │                 ╱            ⎟
   └─────────┬───────┬─────┬─────┬──────────
          4.2      4.8   5.1   5.7       6.3
         MHWN                           MHWS

Result: 2.0 knots
```

---

#### Example 2: Near-Neap Conditions

**Given**:
- Neap: 0.8 knots, Spring: 2.4 knots
- Actual range: 3.8m
- MHWN: 3.5m, MHWS: 5.5m

**What to expect**:
- Range (3.8) is very close to MHWN (3.5)
- Result should be close to neap rate
- Position is only 0.3m above neap (15% of 2.0m span)

```
2.4┤                                           •    2.4
   │                                         ╱
2.0┤                                       ╱      2.0
   │                                     ╱
1.6┤                                   ╱          1.6
   │                                 ╱
1.2┤                               ╱              1.2
   │                      [X]    ╱
0.8┤•                      ⎜   ╱                 0.8
   │                       ⎟ ╱
0.4┤                       ⎟╱                    0.4
   │                       ⎟
   └───┬─────┬───────┬─────┬─────┬───────
      3.5   3.8     4.5    5.0   5.5
     MHWN                        MHWS

Result: 1.0 knots (close to neap as expected)
```

---

#### Example 3: Near-Spring Conditions

**Given**:
- Neap: 1.5 knots, Spring: 3.3 knots
- Actual range: 6.2m
- MHWN: 4.5m, MHWS: 6.5m

**What to expect**:
- Range (6.2) is very close to MHWS (6.5)
- Result should be close to spring rate
- Position is only 0.3m below spring (85% of way from neap)

```
3.3┤                                        [X]•    3.3
   │                                        ⎜╱
2.8┤                                        ╱      2.8
   │                                      ╱⎟
2.4┤                                    ╱  ⎟      2.4
   │                                  ╱    ⎟
2.0┤                                ╱      ⎟      2.0
   │                              ╱        ⎟
1.5┤•                           ╱          ⎟      1.5
   │                          ╱            ⎟
1.0┤                        ╱              ⎟      1.0
   │                                       ⎟
   └───┬─────┬───────┬─────┬───┬───┬──────
      4.5   5.0     5.5   6.0 6.2 6.5
     MHWN                          MHWS

Result: 3.1 knots (close to spring as expected)
```

---

#### Example 4: Extrapolation Beyond Spring

**Given**:
- Neap: 1.2 knots, Spring: 2.6 knots
- Actual range: 7.0m
- MHWN: 4.0m, MHWS: 6.0m

**What to expect**:
- Range exceeds MHWS
- Must extend line beyond spring point
- Result will be greater than spring rate

```
3.2┤                                             [X] 3.2
   │                                            ╱
2.8┤                                          ╱│   2.8
   │                                        ╱  ⎟
2.6┤                                    • ╱    ⎟   2.6
   │                                    ╱      ⎟
2.2┤                                  ╱        ⎟   2.2
   │                                ╱          ⎟
1.8┤                              ╱            ⎟   1.8
   │                            ╱              ⎟
1.4┤                          ╱                ⎟   1.4
   │                        ╱                  ⎟
1.2┤•                     ╱                    ⎟   1.2
   │                   ╱                       ⎟
   └───┬─────┬───────┬───────┬───────┬────────
      4.0   4.5     5.0     6.0     7.0
     MHWN                  MHWS   (actual)

Note: Line extends beyond spring (dotted) line
Result: 3.2 knots (greater than spring rate)
```

---

#### Reading Accuracy

**Rate Scale Resolution**:
- Primary marks: every 0.5 knots
- Secondary marks: every 0.1 knot (if shown)
- Read to nearest 0.1 knot
- Estimate between marks if necessary

**Common Reading Errors**:
1. Reading wrong axis (left vs right)
2. Not using ruler for straight line
3. Reading obliquely (parallax error)
4. Misreading 0.1 increments

**Best Practice**:
- Use sharp pencil and ruler
- Draw lines lightly (for erasing)
- Read perpendicular to axes
- Double-check which axis you're reading
- Verify result is sensible (between neap and spring for normal interpolation)

---

#### Alternative Graph Formats

Some almanacs use variations:

**Vertical Format**:
- Range on vertical axis
- Rates on horizontal axis
- Same principle, rotated 90°

**Logarithmic Scale**:
- Rare, for extreme tidal ranges
- Use same plotting method
- Interpolation line may curve slightly

**Dual-Scale**:
- Feet and meters on same graph
- Ensure you read correct scale
- Check almanac legend

**Always check your specific almanac's graph format and legend before use.**
