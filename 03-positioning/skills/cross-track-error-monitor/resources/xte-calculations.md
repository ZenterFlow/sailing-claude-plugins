# XTE Calculation Methods

## Method 1: Graphical (Chart Plotting)

**Steps**:
1. Draw planned track line on chart
2. Mark current position
3. Use parallel rulers to draw perpendicular from position to track
4. Measure distance with dividers

**Most accurate for chart work and exam use**

```
        Track Line (045°T)
          /
         /
        /
       /
      /
     /----┐
    /     │ ← XTE (perpendicular distance)
   /      │
  /      [X] Current Position
 /
/
```

## Method 2: GPS/Chartplotter

**Modern Method**:
- GPS calculates XTE automatically
- Displayed on chartplotter screen
- Updates continuously
- **Verify it makes sense** (sanity check against chart)

**GPS XTE Display**:
```
XTE: 0.15 nm L
     ^^^^     ^
     │        └─ Direction: L=Left (port), R=Right (starboard)
     └────────── Distance off track
```

## Method 3: Mathematical (Advanced)

**For precise calculations** (rarely needed in practice):

Given:
- Track direction: θ (degrees True)
- Start position: (Lat₁, Lon₁)
- Current position: (Lat₂, Lon₂)

Calculate:
1. Bearing from start to current: β
2. Distance from start to current: D
3. Angular difference: Δθ = β - θ
4. XTE = D × sin(Δθ)

**Sign convention**:
- Positive XTE = starboard of track
- Negative XTE = port of track

## Method 4: Distance/Bearing Check

**Quick Approximation**:
1. Measure distance along track (from start)
2. Measure distance to current position (from start)
3. If distances very different → significant XTE

**Example**:
- Expected: 10 nm along track (045°T)
- Actual: 050°T bearing, 10.5 nm distance
- → XTE ≈ 0.5 nm starboard (rough estimate)

## Method 5: Waypoint Method (GPS)

**Using Waypoints**:
1. Set waypoint at destination
2. Activate "Go To" on GPS
3. GPS shows:
   - Bearing to waypoint
   - Distance to waypoint
   - XTE from track

**Important**: Track line is direct line from current position to waypoint

## Worked Example

**Scenario**:
- Planned track: 090°T
- Start: 50°00'N, 005°00'W
- Current: 50°00'N, 004°50'W
- Question: What is XTE?

**Graphical Solution**:
1. Plot start position
2. Draw line 090°T (due East)
3. Plot current position
4. Current position is ON the track line (same latitude, moved east)
5. **XTE = 0 nm** (perfect tracking!)

**Second Example**:
- Planned track: 090°T
- Start: 50°00'N, 005°00'W
- Current: 50°05'N, 004°50'W
- Question: XTE?

**Solution**:
1. Plot both positions
2. Current is 5 nm NORTH of track
3. Perpendicular distance = 5 nm
4. Direction: STARBOARD (north is to right of eastward track)
5. **XTE = 5.0 nm to starboard**

## XTE vs Distance to Waypoint

**Key Difference**:

```
         Waypoint (W)
            /│\
           / │ \
          /  │  \
         /   │   \  ← Distance to Waypoint
        /    │XTE \   (slant range)
       /     │     \
      /      │      \
     /       │       \
    /        │        \
   /─────────┼─────────\
Start       Track    Current
           Line        Position (X)

XTE = perpendicular distance to track line
Distance to waypoint = direct distance from X to W
```

**They are NOT the same!**

## Monitoring Tips

1. **Set XTE alarm on GPS** (e.g., 0.2 nm for TSS)
2. **Log XTE every hour** in deck log
3. **Plot positions regularly** to visualize trend
4. **Check XTE direction** (which way are you drifting?)
5. **Correlate with wind/stream** (understand cause)

## Correction Strategy

**Gradual Correction** (preferred):
```
    Track
     │
     │  XTE = 0.3 nm
     │        /
     │       /
     │      /  ← Gradual return (alter 5°)
     │     /
     │    /
     │   / Current
     │  /  Position
     │ /
     │/
```

**Aggressive Correction** (risks overshoot):
```
    Track
     │
     │  XTE = 0.3 nm
     │    │
     │    │  ← Direct return (alter 15°)
     │    │
     │    │
     │    │ Current
     │    │ Position
     │    │
```

**Recommended**:
- Small XTE: Gradual correction (3-5°)
- Medium XTE: Moderate correction (5-10°)
- Large XTE: Urgent correction (10-15°)
- Monitor result and adjust
