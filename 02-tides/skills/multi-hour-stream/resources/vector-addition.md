### Vector Addition for Tidal Stream Integration

#### What is a Vector?

A **vector** has both:
- **Magnitude** (size/length/distance)
- **Direction** (bearing/angle)

For tidal streams:
- Magnitude = distance tide moves you (rate × time)
- Direction = set of tide (True bearing)

**Example**: "2.5 knots at 090°T for 1 hour" = Vector of 2.5 NM at 090°T

#### Graphical Vector Addition (Tip-to-Tail Method)

**Method**:
1. Draw first vector from origin
2. Draw second vector from tip of first
3. Draw third vector from tip of second
4. Continue for all vectors
5. Draw resultant from origin to final tip

**Example**: Three vectors

```
Vector A: 3 NM at 045°T
Vector B: 2 NM at 090°T
Vector C: 1 NM at 060°T

         N
         ↑
         │     C →
         │    ↗
         │  B →
         ↗
       A ────────→ E
    Origin

Resultant: From origin to end of C
```

**Scale**: Use any convenient scale
- 1 cm = 1 NM
- 1 inch = 2 NM
- Whatever fits your paper

**Tools needed**:
- Portland plotter or protractor
- Ruler with nautical mile scale
- Pencil and paper
- Optional: plotting sheet

#### Mathematical Vector Addition (Component Method)

**Principle**: Break each vector into North/South and East/West components

**Formulas**:
```
For vector with distance D at angle θ (from North):

North component = D × cos(θ)
East component  = D × sin(θ)
```

**Sign conventions**:
- North: positive (+)
- South: negative (-)
- East: positive (+)
- West: negative (-)

**Process**:
1. Convert each vector to components
2. Sum all North components
3. Sum all East components
4. Calculate resultant from sums

**Resultant formulas**:
```
Resultant Distance = √((ΣNorth)² + (ΣEast)²)
Resultant Direction = arctan(ΣEast / ΣNorth)
```

**Quadrant corrections** (for arctan result):

| ΣNorth | ΣEast | Quadrant | True Bearing |
|--------|-------|----------|--------------|
| +      | +     | NE       | θ |
| -      | +     | SE       | 180° - θ |
| -      | -     | SW       | 180° + θ |
| +      | -     | NW       | 360° - θ |

Where θ = arctan(|ΣEast / ΣNorth|)

Or use **atan2** function (handles quadrants automatically):
```
Direction = atan2(ΣEast, ΣNorth)
```

#### Worked Example: Three Vectors

**Given**:
- Vector 1: 2.0 NM at 060°T
- Vector 2: 1.5 NM at 120°T
- Vector 3: 1.0 NM at 090°T

**Step 1: Components**

Vector 1 (2.0 NM @ 060°):
```
North: 2.0 × cos(60°) = 2.0 × 0.500 = 1.00 NM
East:  2.0 × sin(60°) = 2.0 × 0.866 = 1.73 NM
```

Vector 2 (1.5 NM @ 120°):
```
North: 1.5 × cos(120°) = 1.5 × (-0.500) = -0.75 NM
East:  1.5 × sin(120°) = 1.5 × (0.866)  = 1.30 NM
```

Vector 3 (1.0 NM @ 090°):
```
North: 1.0 × cos(90°) = 1.0 × 0.000 = 0.00 NM
East:  1.0 × sin(90°) = 1.0 × 1.000 = 1.00 NM
```

**Step 2: Sum components**
```
ΣNorth = 1.00 + (-0.75) + 0.00 = 0.25 NM
ΣEast  = 1.73 + 1.30 + 1.00    = 4.03 NM
```

**Step 3: Calculate resultant**
```
Distance = √((0.25)² + (4.03)²)
        = √(0.06 + 16.24)
        = √16.30
        = 4.04 NM

Direction = arctan(4.03 / 0.25)
         = arctan(16.12)
         = 86.5°

Both positive (NE quadrant) → 087°T
```

**Answer**: Resultant = 4.0 NM at 087°T

#### Quick Reference: Common Angles

| Angle | cos(θ) | sin(θ) | Notes |
|-------|--------|--------|-------|
| 0° (N) | 1.000 | 0.000 | All North |
| 30° | 0.866 | 0.500 | NNE |
| 45° (NE) | 0.707 | 0.707 | Equal N & E |
| 60° | 0.500 | 0.866 | ENE |
| 90° (E) | 0.000 | 1.000 | All East |
| 120° | -0.500 | 0.866 | ESE |
| 135° (SE) | -0.707 | 0.707 | Equal S & E |
| 150° | -0.866 | 0.500 | SSE |
| 180° (S) | -1.000 | 0.000 | All South |
| 210° | -0.866 | -0.500 | SSW |
| 225° (SW) | -0.707 | -0.707 | Equal S & W |
| 240° | -0.500 | -0.866 | WSW |
| 270° (W) | 0.000 | -1.000 | All West |
| 300° | 0.500 | -0.866 | WNW |
| 315° (NW) | 0.707 | -0.707 | Equal N & W |
| 330° | 0.866 | -0.500 | NNW |

#### Calculator Usage

**If your calculator has trig functions**:

1. Make sure it's in **degree mode** (not radians)
2. For cos: Enter angle, press COS
3. For sin: Enter angle, press SIN
4. For arctan: Enter value, press TAN⁻¹ or ATAN

**Check**: cos(60°) should give 0.5
- If you get 0.866, calculator is in radians!
- Switch to degree mode

**atan2 function** (if available):
```
atan2(east, north) gives direction directly
No quadrant correction needed
Result in degrees from North
```

#### Verification Methods

**Check 1: Parallel vectors**
If all vectors point same direction (e.g., all 090°):
- Resultant should equal sum of magnitudes
- Resultant direction = vector direction

Example:
```
2 NM @ 090° + 3 NM @ 090° + 1 NM @ 090°
= 6 NM @ 090° ✓
```

**Check 2: Opposing vectors**
If vectors oppose (e.g., 090° and 270°):
- Resultant should equal difference
- Direction = larger vector's direction

Example:
```
5 NM @ 090° + 3 NM @ 270°
= 2 NM @ 090° ✓
```

**Check 3: Right angle vectors**
If two vectors at 90° to each other:
- Use Pythagoras: R = √(A² + B²)

Example:
```
3 NM @ 000° (N) + 4 NM @ 090° (E)
= √(3² + 4²) = √(9 + 16) = √25 = 5 NM
Direction = arctan(4/3) = 53° ✓
```

**Check 4: Equal vectors at 90°**
If two equal vectors at right angles:
- Resultant = Vector × √2 ≈ Vector × 1.414
- Direction = midway between (45°)

Example:
```
2 NM @ 000° + 2 NM @ 090°
= 2 × 1.414 = 2.8 NM @ 045° ✓
```

#### Common Errors

**Error 1: Wrong angle reference**
```
Wrong: Measuring from East (like unit circle)
Right: Measuring from North (nautical convention)
```

**Error 2: Forgetting signs**
```
Wrong: cos(120°) = 0.5
Right: cos(120°) = -0.5 (negative!)
```

**Error 3: Wrong quadrant**
```
If North is negative and East is positive:
You're in SE quadrant (90-180°)
Don't report as NE!
```

**Error 4: Radian mode**
```
If cos(60) gives -0.95... your calculator is in radians!
Switch to degrees
```

**Error 5: Adding magnitudes instead of vectors**
```
Wrong: 2 kn + 3 kn = 5 kn (only true if same direction)
Right: Must add as vectors considering directions
```

#### Special Cases

**Case 1: One vector is zero**
```
Result = other vector(s)
Zero vector contributes nothing
Common at slack water
```

**Case 2: All vectors cancel out**
```
If ΣNorth = 0 and ΣEast = 0
Resultant = 0 (no net drift)
Rare but possible if streams perfectly oppose
```

**Case 3: Very small resultant**
```
If resultant < 0.1 NM
May be negligible for navigation
But still plot if passage >5 hours
```

#### Integration Order

**Important**: You can add vectors in ANY order!

```
A + B + C = C + A + B = B + C + A

All give same resultant.
```

But for tidal streams, use **chronological order** to:
- Match time progression
- Avoid confusion
- Easier to check work

#### Tools and Resources

**On boat**:
- Portland plotter
- Protractor and ruler
- Plotting sheet
- Calculator with trig functions
- Pencil and eraser

**Pre-passage planning**:
- Navigation software
- Spreadsheet for calculations
- Chart plotter (some can integrate)
- Paper backup always!

**Learning**:
- Practice with known answers
- Check graphical vs mathematical
- They should match within 0.1 NM and 1°
