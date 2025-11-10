### Trigonometry Reference for Navigation

#### Basic Trigonometric Functions

**Definitions** (for angle θ in right triangle):

```
         Opposite
           |
           |  / Hypotenuse
           | /
           |/ θ
    ───────────
      Adjacent

sin(θ) = Opposite / Hypotenuse
cos(θ) = Adjacent / Hypotenuse
tan(θ) = Opposite / Adjacent
```

**For navigation** (angle from North):

```
           N (0°)
           ↑
           │ North component
           │
           │ / Vector
           │/ θ
    ───────┼───────→ E (90°)
           │ East component
           │
```

**Vector components**:
```
North = Distance × cos(θ)
East  = Distance × sin(θ)
```

#### Nautical vs Mathematical Conventions

**Mathematical (unit circle)**:
- 0° is East
- Angles measured counter-clockwise
- Used in most calculators

**Nautical (compass)**:
- 0° is North
- Angles measured clockwise
- Used in navigation

**Conversion**: We use nautical convention throughout.

#### Trigonometric Values Table

**Cardinal and Intercardinal Points**:

| Direction | Angle | cos(θ) | sin(θ) | tan(θ) |
|-----------|-------|--------|--------|--------|
| N | 000° | 1.000 | 0.000 | 0.000 |
| NNE | 022.5° | 0.924 | 0.383 | 0.414 |
| NE | 045° | 0.707 | 0.707 | 1.000 |
| ENE | 067.5° | 0.383 | 0.924 | 2.414 |
| E | 090° | 0.000 | 1.000 | ∞ |
| ESE | 112.5° | -0.383 | 0.924 | -2.414 |
| SE | 135° | -0.707 | 0.707 | -1.000 |
| SSE | 157.5° | -0.924 | 0.383 | -0.414 |
| S | 180° | -1.000 | 0.000 | 0.000 |
| SSW | 202.5° | -0.924 | -0.383 | 0.414 |
| SW | 225° | -0.707 | -0.707 | 1.000 |
| WSW | 247.5° | -0.383 | -0.924 | 2.414 |
| W | 270° | 0.000 | -1.000 | ∞ |
| WNW | 292.5° | 0.383 | -0.924 | -2.414 |
| NW | 315° | 0.707 | -0.707 | -1.000 |
| NNW | 337.5° | 0.924 | -0.383 | -0.414 |

**Common Navigation Angles** (5° intervals):

| Angle | cos | sin | Angle | cos | sin |
|-------|-----|-----|-------|-----|-----|
| 000° | 1.000 | 0.000 | 180° | -1.000 | 0.000 |
| 005° | 0.996 | 0.087 | 185° | -0.996 | -0.087 |
| 010° | 0.985 | 0.174 | 190° | -0.985 | -0.174 |
| 015° | 0.966 | 0.259 | 195° | -0.966 | -0.259 |
| 020° | 0.940 | 0.342 | 200° | -0.940 | -0.342 |
| 025° | 0.906 | 0.423 | 205° | -0.906 | -0.423 |
| 030° | 0.866 | 0.500 | 210° | -0.866 | -0.500 |
| 035° | 0.819 | 0.574 | 215° | -0.819 | -0.574 |
| 040° | 0.766 | 0.643 | 220° | -0.766 | -0.643 |
| 045° | 0.707 | 0.707 | 225° | -0.707 | -0.707 |
| 050° | 0.643 | 0.766 | 230° | -0.643 | -0.766 |
| 055° | 0.574 | 0.819 | 235° | -0.574 | -0.819 |
| 060° | 0.500 | 0.866 | 240° | -0.500 | -0.866 |
| 065° | 0.423 | 0.906 | 245° | -0.423 | -0.906 |
| 070° | 0.342 | 0.940 | 250° | -0.342 | -0.940 |
| 075° | 0.259 | 0.966 | 255° | -0.259 | -0.966 |
| 080° | 0.174 | 0.985 | 260° | -0.174 | -0.985 |
| 085° | 0.087 | 0.996 | 265° | -0.087 | -0.996 |
| 090° | 0.000 | 1.000 | 270° | 0.000 | -1.000 |
| 095° | -0.087 | 0.996 | 275° | 0.087 | -0.996 |
| 100° | -0.174 | 0.985 | 280° | 0.174 | -0.985 |
| 105° | -0.259 | 0.966 | 285° | 0.259 | -0.966 |
| 110° | -0.342 | 0.940 | 290° | 0.342 | -0.940 |
| 115° | -0.423 | 0.906 | 295° | 0.423 | -0.906 |
| 120° | -0.500 | 0.866 | 300° | 0.500 | -0.866 |
| 125° | -0.574 | 0.819 | 305° | 0.574 | -0.819 |
| 130° | -0.643 | 0.766 | 310° | 0.643 | -0.766 |
| 135° | -0.707 | 0.707 | 315° | 0.707 | -0.707 |
| 140° | -0.766 | 0.643 | 320° | 0.766 | -0.643 |
| 145° | -0.819 | 0.574 | 325° | 0.819 | -0.574 |
| 150° | -0.866 | 0.500 | 330° | 0.866 | -0.500 |
| 155° | -0.906 | 0.423 | 335° | 0.906 | -0.423 |
| 160° | -0.940 | 0.342 | 340° | 0.940 | -0.342 |
| 165° | -0.966 | 0.259 | 345° | 0.966 | -0.259 |
| 170° | -0.985 | 0.174 | 350° | 0.985 | -0.174 |
| 175° | -0.996 | 0.087 | 355° | 0.996 | -0.087 |

#### Inverse Functions

**Finding angle from ratio**:

```
If sin(θ) = x, then θ = arcsin(x) or sin⁻¹(x)
If cos(θ) = x, then θ = arccos(x) or cos⁻¹(x)
If tan(θ) = x, then θ = arctan(x) or tan⁻¹(x)
```

**For resultant direction** from components:

```
θ = arctan(East / North)
```

**Quadrant correction needed!**

#### Quadrant Determination

**From component signs**:

```
         N (+)
          ↑
          │
    (-) ──┼── (+) E
    W     │
          │
         S (-)

Quadrant I (NE):   North +, East +  → θ = arctan(E/N)
Quadrant II (SE):  North -, East +  → θ = 180° - arctan(E/N)
Quadrant III (SW): North -, East -  → θ = 180° + arctan(E/N)
Quadrant IV (NW):  North +, East -  → θ = 360° - arctan(E/N)
```

**Alternative: atan2 function**

Many calculators and programming languages have atan2:

```
θ = atan2(East, North)
```

This automatically handles quadrants. Result is -180° to +180°.

**Convert atan2 result to nautical bearing**:
```
If atan2 result < 0: Add 360°
```

#### Practical Examples

**Example 1**: Vector 3.5 NM at 065°T

```
North = 3.5 × cos(65°) = 3.5 × 0.423 = 1.48 NM
East  = 3.5 × sin(65°) = 3.5 × 0.906 = 3.17 NM
```

**Example 2**: Components to bearing

```
North = -2.5 NM (negative = south)
East  = +3.0 NM (positive = east)

Magnitude = √((-2.5)² + (3.0)²)
         = √(6.25 + 9.00)
         = √15.25
         = 3.9 NM

Direction = arctan(3.0 / -2.5)
         = arctan(-1.2)
         = -50.2°

Quadrant: N-, E+ = SE (Quadrant II)
True bearing = 180° - 50.2° = 129.8° ≈ 130°T

Answer: 3.9 NM at 130°T
```

#### Special Angles (Worth Memorizing)

**30-60-90 Triangle**:
```
sin(30°) = cos(60°) = 0.5
sin(60°) = cos(30°) = 0.866
tan(30°) = 0.577
tan(60°) = 1.732
```

**45-45-90 Triangle**:
```
sin(45°) = cos(45°) = 0.707 (= 1/√2)
tan(45°) = 1.000
```

#### Pythagorean Theorem

**For right triangles**:
```
c² = a² + b²

Where c is hypotenuse (longest side)
```

**For resultant vectors**:
```
Resultant = √((North component)² + (East component)²)
```

**Example**:
```
North = 4.0 NM
East = 3.0 NM

Resultant = √(4.0² + 3.0²)
         = √(16 + 9)
         = √25
         = 5.0 NM

Classic 3-4-5 triangle!
```

#### Distance Formula (Cartesian)

**Between two points**:
```
Distance = √((N₂ - N₁)² + (E₂ - E₁)²)
```

**For navigation**: This is how EP is calculated from fix + water track + tide.

#### Common Approximations

**Small angle approximations** (angles < 10°):
```
sin(θ) ≈ tan(θ) ≈ θ (in radians)
cos(θ) ≈ 1

1 degree = 0.01745 radians
```

**Useful for**:
- Course corrections
- Small tidal set angles
- Leeway estimates

**Not accurate enough for**:
- Tidal stream integration (use full trig)
- Long passage calculations
- Any bearing > 10°

#### Calculator Tips

**Ensure degree mode**:
```
Test: cos(60) should give 0.5
If you get -0.952, you're in radian mode!
```

**Mode switching**:
- Usually button labeled "DRG" or "MODE"
- D = Degrees, R = Radians, G = Gradians
- Choose Degrees

**Common calculator functions**:
- `COS`, `SIN`, `TAN`: Direct functions
- `ACOS`, `ASIN`, `ATAN`: Inverse functions
- `√`: Square root
- `x²`: Square
- `π`: Pi (3.14159...)

**Order of operations**:
```
Calculate: 3.5 × cos(65°)

Press: 3.5 × 65 cos =
OR: cos 65 × 3.5 =

Depends on calculator type!
```

#### Mental Calculation Tricks

**For 45° (NE, SE, SW, NW)**:
```
Components are equal
North = East = Distance × 0.707
Quick: Multiply by 0.7 for approximation
```

**For 30° and 60°**:
```
30°: cos ≈ 0.9, sin = 0.5 (half)
60°: cos = 0.5 (half), sin ≈ 0.9
```

**For 90° (E, W)**:
```
North component = 0
East component = full distance
```

**For 0° or 180° (N, S)**:
```
East component = 0
North component = full distance (+ or -)
```

#### Verification Methods

**Check 1**: Components should be smaller than original distance
```
If vector is 5 NM, components should be ≤ 5 NM
If you get 6 NM component → ERROR!
```

**Check 2**: Pythagoras check
```
√(North² + East²) should equal original distance
```

**Check 3**: Angle sense check
```
If vector points NE (045°):
- North component should be positive
- East component should be positive
- Both should be roughly equal

If they're not → ERROR in calculation or quadrant
```

**Check 4**: Sign check
```
North component: + if N, - if S
East component:  + if E, - if W

Any time you get unexpected sign → recheck
```

#### Common Errors

1. **Wrong mode** (radians instead of degrees)
2. **Wrong reference** (measuring from East instead of North)
3. **Forgot negative signs** for S or W components
4. **Wrong quadrant** in final answer
5. **Mixing up sin and cos**
6. **Order of operations** error on calculator

**Always double-check your trig calculations!**
