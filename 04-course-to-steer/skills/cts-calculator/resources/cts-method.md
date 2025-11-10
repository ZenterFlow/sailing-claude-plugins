# Course To Steer (CTS) Method

## The Water Triangle

```
       Start Position
            │
            │ Heading (what you point at)
            │
            ↓
        Leeway Effect
            │
            ↓
        Water Track (course through water)
            │
            ↓
        Tidal Stream Effect
            │
            ↓
        Track Made Good (where you actually go)
            │
            ↓
       Destination
```

## Vector Solution Order

**PLANNING (CTS)**: Work BACKWARDS from destination
1. Desired track (where you want to go)
2. Remove tidal effect (plot against stream)
3. Calculate water track needed
4. Remove leeway (calculate heading)
5. Convert to compass (apply variation, deviation)

**PLOTTING (EP)**: Work FORWARDS from position
1. Course steered
2. Add leeway → water track
3. Add stream → track made good

## Step-by-Step CTS Calculation

### Given
- Desired Track Made Good (TMG): θ_TMG
- Boat speed: V_boat
- Stream set/drift: θ_stream @ V_stream
- Leeway: L (degrees)
- Variation: VAR
- Deviation: DEV

### Step 1: Plot Tidal Vector (Backwards)
From destination or reference point:
- Plot RECIPROCAL of stream: θ_stream ± 180°
- Distance: V_stream × time
- Mark endpoint

### Step 2: Find Water Track
From start to tidal-corrected endpoint:
- Measure bearing: θ_water
- Measure distance: d_water

### Step 3: Apply Leeway
Leeway is downwind:
- Wind on PORT: θ_heading = θ_water - L
- Wind on STARBOARD: θ_heading = θ_water + L

### Step 4: Convert to Compass
- Magnetic: θ_M = θ_T - VAR (if VAR is West)
- Compass: θ_C = θ_M - DEV (if DEV is West)

**CADET**: Compass Add East for True

### Step 5: Calculate SOG
Using cosine rule or vector addition:
- Speed Over Ground may be higher or lower than boat speed
- Depends on stream direction relative to track

## Worked Example

**Problem**:
Make good 045°T at 5 kts boat speed
Stream: 090°T @ 2 kts (East)
Leeway: 5° (wind from South, starboard tack)
Variation: 4°W, Deviation: 2°W

**Solution**:

**Step 1: Tidal Vector**
- Stream 090°T @ 2 kts
- For 1-hour plot: 270°T (reciprocal) for 2 nm
- (Plotting AGAINST stream)

**Step 2: Water Track**
- From start, bearing to tidal-corrected point
- Result: ~030°T (more northerly than desired 045°T)
- Distance: ~5.5 nm

**Step 3: Leeway**
- Wind from S (starboard tack)
- Add leeway: 030° + 5° = 035°T heading

**Step 4: Convert**
- True: 035°T
- Magnetic: 035° - 4° = 031°M
- Compass: 031° - 2° = 029°C

**Answer**: Steer 029°C to make good 045°T

## Graphical Method (Chart)

1. Mark start and destination
2. From destination, plot stream BACKWARDS
3. Set compass to boat speed radius
4. Arc from start to intersect stream line
5. Intersection point shows water track endpoint
6. Measure bearing from start to intersection = water track
7. Apply leeway to get heading
8. Convert to compass

## When CTS Fails

**Stream Too Strong**:
If stream perpendicular to track exceeds boat speed component:
- Cannot make desired track
- Will be set sideways
- Options: wait for tide, motor, alter destination

**Example**:
Desired: 000°T (North)
Stream: 090°T @ 6 kts (East)
Boat speed: 5 kts

→ Boat cannot overcome 6 kt eastward stream
→ Will be set east regardless of heading
→ Must wait for tide change or motor

## Quick Estimates

**Small Stream** (<20% of boat speed):
CTS ≈ Direct course ± small correction (2-5°)

**Moderate Stream** (20-50% of boat speed):
CTS ≈ Direct course ± moderate correction (5-15°)

**Strong Stream** (>50% of boat speed):
CTS ≈ Significantly different from direct course
→ Full calculation essential
