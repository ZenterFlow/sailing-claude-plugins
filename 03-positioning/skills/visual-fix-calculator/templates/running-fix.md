# Running Fix Worked Example

## When to Use Running Fix
- Only **one suitable object** available for bearings
- Can't get simultaneous bearings to multiple objects
- Useful along coastline or in channels

## Scenario
Vessel passing a lighthouse:
- **First bearing**: 045°C at 10:00
- **Second bearing**: 090°C at 10:20
- **Course steered**: 180°T
- **Speed**: 6 knots
- **Leeway**: 5° (making good 185°T)
- **Tidal stream**: Negligible

Compass deviation: 2°W
Magnetic variation: 3°E

## Step 1: Convert First Bearing to True

Time: 10:00
Compass bearing to lighthouse: 045°C
True = 045° - 2° + 3° = **046°T**
Reciprocal from lighthouse: **226°T**

## Step 2: Calculate Distance Run

Time between bearings: 20 minutes = 0.33 hours
Speed: 6 knots
Distance: 6 × 0.33 = **2.0 nm**

## Step 3: Advance First Position Line

1. Plot first position line from lighthouse: 226°T
2. Choose any point on this line
3. From that point, draw course made good: 185°T
4. Measure distance along course: 2.0 nm
5. From endpoint, draw new line **parallel** to first position line (226°T)

This is the **transferred position line** (label it "TPL 10:00-10:20")

## Step 4: Plot Second Bearing

Time: 10:20
Compass bearing to lighthouse: 090°C
True = 090° - 2° + 3° = **091°T**
Reciprocal from lighthouse: **271°T**

Plot this line from lighthouse at 271°T

## Step 5: Find Fix Position

**Running fix position**: Where second bearing intersects transferred position line

Measured position: **50°40.2'N, 001°18.5'W** at 10:20

## Step 6: Check Using Four-Point Bearing

**Four-point bearing rule** (special case check):
- First bearing: 045° (4 points on bow)
- Second bearing: 090° (abeam)
- Distance run should equal distance off when abeam

Distance run: 2.0 nm
Distance off (measure perpendicular from fix to lighthouse): ~2.0 nm ✓

**Verification passed!**

## Step 7: Quality Assessment

⚠ **FIX QUALITY: ACCEPTABLE (but less accurate than three-point fix)**

**Limitations**:
- Accumulated errors in course and speed
- Helmsman errors over 20 minutes
- Leeway estimation errors
- Any tidal stream errors
- Compass error affects both bearings

**Accuracy**: Typically ±0.3-0.5 nm

**Recommendation**:
- Use for general navigation
- **DO NOT use** for critical pilotage
- Update with three-point fix when possible

## Special Cases

### Doubling the Angle on the Bow
If second angle = 2 × first angle:
- Distance off at second bearing = distance run

Example:
- First: 030° on bow
- Second: 060° on bow
- Run 4 nm between bearings
- → Distance off = 4 nm when at second bearing

### Four-Point Bearing (45°-90°)
If bearings are 45° then 90°:
- Distance off when abeam = distance run

### Special Angle Fix (26.5°-45°-63.5°)
- When at 26.5°: run distance = 2× distance off
- When at 45°: run distance = distance off
- When at 63.5°: distance off = 2× run distance

## Common Errors

1. **Forgetting to transfer position line** (plotting from wrong time)
2. **Not advancing in direction of CMG** (using heading instead of actual track)
3. **Errors in distance calculation** (wrong time interval or speed)
4. **Not accounting for leeway and stream** (use Course Made Good, not heading)

## Best Practices

- Take bearings at convenient angles when possible (45°, 90°, 4-point)
- Note exact time of each bearing
- Steer steady course between bearings
- Maintain constant speed
- Check log reading or GPS distance for verification
- Use prominent, unmistakable objects
- Update running fix frequently (every 20-30 mins max)
