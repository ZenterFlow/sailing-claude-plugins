# Light Ranges and Radar Beacons

---
name: light-ranges-beacons
version: 1.0.0
triggers:
  - "light range"
  - "geographical range"
  - "nominal range"
  - "luminous range"
  - "dipping distance"
  - "RACON"
  - "radar beacon"
---

## Purpose

Calculate and apply light visibility ranges including geographical, luminous, and nominal ranges, and identify radar beacons (RACON) for electronic navigation assistance.

## Activation Triggers

This skill activates when you ask about:
- Light range calculations or visibility
- Geographical vs luminous vs nominal range
- Dipping distance calculations
- When lights should become visible
- RACON identification on radar

## Behavior

### Types of Light Range

Understanding three distinct range concepts is critical for navigation:

**1. Geographical Range**

- **Definition**: Extreme distance based on line of sight (Earth's curvature limitation)
- **Factors**: Height of eye, height of light, weather clarity
- **Formula**: 2.08 × √height of eye + 2.08 × √height of light (in nautical miles)
- **Use**: Calculate when light should become visible when approaching
- **Limitation**: Assumes clear weather; may see further in exceptional conditions

**2. Luminous Range**

- **Definition**: Greatest distance visible based on light intensity and atmospheric visibility
- **Factors**: Luminous intensity of light, atmospheric clarity
- **Variable**: Changes dramatically with weather conditions
- **Reality**: Reduces in fog, haze, rain, or poor visibility

**3. Nominal Range**

- **Definition**: Luminous range standardized for visibility of 10 nautical miles (meteorological visibility)
- **Chart Information**: Usually listed as "Visible up to X miles" or "XM"
- **Standard**: All nominal ranges assume 10nm visibility
- **Reduction**: Decreases proportionally as visibility reduces below 10 miles
- **Example**: "15M" means 15 mile nominal range in 10nm visibility

### The Practical Range Concept

**Reality**: The limiting factor is whichever is **shorter**:
- Geographical range (curvature), OR
- Luminous range (weather)

**Example**:
- Large vessel (10m height of eye) sees 24M light at greater range than small vessel (2m height of eye)
- But in 5nm visibility, neither vessel sees the full geographical range

### Dipping Distance Calculation

**Formula**:
```
Distance (nm) = 2.08 × √(Height of Eye in meters) + 2.08 × √(Height of Light in meters)
```

**Components**:
- First term: Distance to horizon from vessel
- Second term: Distance from light to its horizon
- Sum: Total visible distance

**Example Calculation**:
- Height of eye: 4 meters
- Light height: 25 meters
- Distance = 2.08 × √4 + 2.08 × √25
- Distance = 2.08 × 2 + 2.08 × 5
- Distance = 4.16 + 10.4 = **14.56 nautical miles**

### Using Dipping Distance for Position Fixing

**Method**:
1. Obtain light height from chart or almanac
2. Estimate height of eye on your vessel (bridge/cockpit level)
3. Apply formula or use pre-calculated tables
4. Take bearing when light first appears on horizon
5. Plot position line at calculated distance

**Important**: Add height of tide to light height for accuracy

### RACON (Radar Beacon)

**Definition**: Transponder beacon transmitting coded signal on radar frequency

**Function**: Permits interrogating craft to determine bearing and range to beacon

**Frequencies**:
- **3cm (X-band)**: 9300-9500 MHz (most common on yachts)
- **10cm (S-band)**: 2900-3100 MHz (commercial vessels)

**Radar Display**: Appears as Morse code pattern extending radially from beacon position

**Identification**:
- Morse character appears at same range as RACON
- Examples: "T" (—), "O" (— — —), "M" (— —)
- Pattern extends outward from actual position

**Chart Symbol**: Racon with associated Morse letter

**Use**:
- Identify specific navigation mark on radar
- Verify position in poor visibility
- Confirm radar range calibration

### Light Visibility Table Reference

Quick reference for heights and ranges:

| Height of Eye | Horizon Distance | Light at 20m | Light at 40m |
|---------------|------------------|--------------|--------------|
| 2m | 2.9nm | 16.1nm | 19.2nm |
| 4m | 4.2nm | 17.4nm | 20.5nm |
| 6m | 5.1nm | 18.3nm | 21.4nm |
| 10m | 6.6nm | 19.8nm | 22.9nm |

### Common Errors to Avoid

❌ Confusing geographical vs luminous vs nominal range
❌ Using nominal range as guaranteed visibility distance
❌ Forgetting to add height of tide for light height calculations
❌ Misidentifying RACON Morse code on radar
❌ Not accounting for reduced visibility in fog/haze
❌ Assuming you'll always see the nominal range listed

### Assessment Criteria

You should be able to:
- Calculate dipping distance for given heights
- Explain difference between three range types
- Determine when specific light should become visible
- Identify RACON on radar display
- Apply range knowledge for passage planning
- Adjust expectations based on weather conditions

### Practical Application

**Scenario**: Planning approach to harbor with 30m lighthouse, nominal range 18M

**Your vessel**: Height of eye 3m, visibility 8nm

1. **Geographical range**: 2.08 × √3 + 2.08 × √30 = 3.6 + 11.4 = **15nm**
2. **Nominal range**: 18M (but assumes 10nm visibility)
3. **Actual visibility**: 8nm (worse than standard)
4. **Limiting factor**: Weather visibility (8nm) limits you, not geography
5. **Expectation**: See light at approximately **8nm** maximum

**Scenario**: Using RACON for position fix in fog

1. **Radar**: Shows Morse "T" (—) pattern at 5.2nm bearing 045°T
2. **Chart**: Confirms RACON(T) at entrance buoy
3. **Action**: Plot position 5.2nm at 225°T from buoy
4. **Confidence**: High - RACON provides accurate range/bearing

---

**Version**: 1.0.0 (v1.0.0 - 2025-11-10)
