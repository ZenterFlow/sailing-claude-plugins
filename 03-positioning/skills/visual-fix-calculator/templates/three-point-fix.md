# Three-Point Fix Worked Example

## Scenario
Vessel taking three compass bearings:
- **Object A** (Lighthouse): 045°C
- **Object B** (Church spire): 135°C
- **Object C** (Water tower): 200°C

Compass deviation: 3°W
Magnetic variation: 4°E (from chart)

## Step 1: Convert Compass to True Bearings

**Formula**: True = Compass + Deviation + Variation
*Remember*: East is positive, West is negative

| Object | Compass | Deviation | Variation | True Bearing |
|--------|---------|-----------|-----------|--------------|
| A (Lighthouse) | 045°C | -3° | +4° | **046°T** |
| B (Church) | 135°C | -3° | +4° | **136°T** |
| C (Tower) | 200°C | -3° | +4° | **201°T** |

## Step 2: Calculate Reciprocals (for plotting FROM objects)

| Object | True Bearing | Reciprocal (±180°) |
|--------|--------------|-------------------|
| A | 046°T | **226°T** |
| B | 136°T | **316°T** |
| C | 201°T | **021°T** |

## Step 3: Check Bearing Geometry

Angles between bearings:
- A to B: 136° - 046° = **90°** ✓ EXCELLENT
- B to C: 201° - 136° = **65°** ✓ GOOD
- C to A: (360° - 201°) + 046° = **205°** (complementary 155°) ✗ ACCEPTABLE

**Assessment**: Good overall geometry (one excellent, one good, one acceptable)

## Step 4: Plot Position Lines

Plot from chart:
1. From Lighthouse: draw line 226°T
2. From Church: draw line 316°T
3. From Tower: draw line 021°T

## Step 5: Assess Cocked Hat

Lines form small triangle (cocked hat):
- Size: approximately **0.15 nm** (300 meters)

## Step 6: Determine Position

**Best Position**: Center of cocked hat

Measured position: **50°42.3'N, 001°14.8'W**

## Step 7: Quality Assessment

✓ **FIX QUALITY: GOOD**
- Bearing geometry: Good (two good angles, one acceptable)
- Cocked hat: 0.15 nm (small)
- **Recommendation**: Suitable for coastal navigation
- **Action**: Use this position for plotting

## Alternative: If Cocked Hat Too Large (>0.5 nm)

1. Check for systematic error:
   - Wrong object identified?
   - Deviation/variation incorrect?
   - Compass malfunction?

2. Identify most reliable bearing:
   - Closest object (usually most accurate)
   - Most prominent (lighthouse > church > headland)
   - Ahead or astern (changes slowest)

3. Discard suspect bearing if one clearly off

4. If still large: **RE-TAKE ALL BEARINGS**

## Time Management
- Take all three bearings within **30 seconds**
- Take most reliable bearing **LAST** (it changes slowest)
- Typical sequence:
  1. Fastest-changing bearing (beam)
  2. Medium-changing bearing
  3. Slowest-changing bearing (ahead/astern)

## Plotting Notes
- Always plot **reciprocal** (bearing FROM object TO ship)
- Use **soft pencil** for easy corrections
- Label each position line with object name and time
- Circle the fix position and note time
