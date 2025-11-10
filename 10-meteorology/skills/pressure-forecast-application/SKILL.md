# Atmospheric Pressure Effects and Forecast Application

---
name: pressure-forecast-application
version: 1.0.0
triggers:
  - "pressure effects"
  - "forecast application"
  - "weather routing"
  - "depth pressure"
  - "wind against tide"
  - "almanac weather"
---

## Purpose

Apply atmospheric pressure effects on tidal heights, interpret weather forecasts for navigation decisions, and synthesize multiple data sources for route planning.

## Activation Triggers

This skill activates when you ask about:
- Pressure effects on depth or water level
- Forecast application to navigation
- Weather routing decisions
- Wind against tide conditions
- Almanac weather integration

## Behavior

### Pressure Effects on Water Depth

**Standard Pressure:**
- **UK Standard**: 1013mb (assumed pressure for tide tables)
- **Global Reference**: Average sea level pressure

**Pressure-Depth Relationship:**
- **General Rule**: 1mb above standard = 1cm less water depth
- **Example Calculation**:
  - Pressure: 1035mb
  - Difference: 1035 - 1013 = 22mb
  - Depth Reduction: 22cm less than predicted
- **Critical Thresholds**:
  - >10mb above standard: Significant consideration needed
  - Critical depth situations: Even 5-10cm can matter
- **Low Pressure**: Below 1013mb = deeper water than predicted

**Practical Implications:**
- **Harbor Entry**: High pressure could reduce depth below safe limit
- **Bridge Clearance**: Low pressure increases air draft clearance (usually less critical)
- **Combined Factors**: Pressure is one of many factors - combine with:
  - Tidal state (height of tide)
  - Wind direction and strength
  - Wave/swell conditions

### Forecast Interpretation for Navigation

**Forecast Sources and Uses:**

**Synoptic Charts:**
- **Scale**: Large area (thousands of miles)
- **Best For**: Medium to long-term planning (3-5+ days)
- **Limitation**: Needs refinement for local sailing
- **Information**: System positions, movement, pressure gradients

**Shipping Forecast:**
- **Scale**: Sea area (regional)
- **Best For**: Short to medium-term planning, offshore passages
- **Validity**: 24 hours typically
- **Information**: Wind, weather, visibility, pressure tendency

**Inshore Waters Forecast:**
- **Scale**: Fixed coastline stretches
- **Best For**: Short-term, local passages
- **Advantage**: Includes local effects
- **Information**: Detailed coastal conditions

**GRIB Files:**
- **Scale**: Varies (100km+ for free versions)
- **Best For**: Long-term offshore planning, trend analysis
- **Limitation**: Not suitable for short-term local decisions
- **Information**: Wind, rain, pressure, wave data

**Mobile App Forecasts (GFS-based):**
- **Scale**: Regional to local
- **Best For**: Supplementing official forecasts
- **Format**: 3-hour blocks (conditions change gradually)
- **Information**: Multiple parameters (wind, rain, temperature)

**Live Observations:**
- **Sources**: ODAS buoys, weather stations, ship reports
- **Best For**: Real-time verification of forecasts
- **Use**: Update synoptic information, confirm conditions

### Weather Routing Applications

**Primary Use**: Determine if conditions suitable for vessel and crew

**Specific Applications**:
1. **Port Selection**: Best shelter for given conditions
2. **Alternative Havens**: Identify ports of refuge
3. **Route Adjustment**: Modify planned route for weather
4. **Departure Timing**: Choose favorable weather window
5. **Tide-Wind Interaction**: Avoid wind-against-tide conditions

### Wind Direction Analysis

**Plot wind direction on chart** to determine angle relative to vessel:
- **Windward (Beat)**: Slowest, most challenging
- **Beam Reach**: Fastest, comfortable sailing
- **Dead Run**: Risk of rolling, seasickness

### Sea State Factors

**Components Affecting Sea Conditions**:

1. **Wind Direction vs Tide Direction:**
   - Same direction = calmer sea
   - Opposite direction = rougher sea

2. **Fetch**: Distance wind travels over water
   - Longer fetch = larger wave height

3. **Depth Proximity:**
   - Offshore wind near shore = calmer
   - Onshore wind near shore = breaking waves, dangerous

4. **Wind-Against-Tide:**
   - Can cause serious seas even in moderate conditions
   - Avoid rounding headlands in these conditions

### Almanac Integration Example

**Scenario**: "After prolonged strong westerly winds, what sea conditions at bar entrance near LW?"

**Analysis Process**:
1. **Consult Almanac**: Locate harbor information (e.g., page 77)
2. **Key Information**: Bar "dangerous at LW with westerly swell"
3. **Specific Warning**: "2m swell offshore generates dangerous breaking swell on bar; do not attempt entry"
4. **Conclusion**: Anchorage "untenable" in westerly swell
5. **Alternative**: Consider nearby alternatives (e.g., bay to north)
6. **Further Check**: Verify alternative's wind exposure
7. **Final Decision**: Select destination based on forecast wind direction

### Forecast Validation Checklist

**Before relying on any forecast, verify**:

1. **Coverage**: Does forecast cover sailing area?
2. **Timeliness**: Issued within last 24 hours?
3. **Scale**: Appropriate for passage type?
4. **Completeness**: All required parameters included?
5. **Cross-Reference**: Multiple sources available?
6. **Local Knowledge**: Consult almanac for area-specific effects

### Almanac Information Types

**Typical contents**:
- Sea areas and forecast regions
- Live observations from ODAS buoys
- Shipping forecast schedule and content
- Inshore forecast areas
- Synoptic chart timing (analysis vs forecast)
- Local port/harbor weather sensitivities
- Specific hazard warnings (bars, overfalls, etc.)

### Common Errors to Avoid

❌ Not considering pressure effects on critical depths
❌ Using non-marine forecasts for navigation decisions
❌ Relying on single forecast source without validation
❌ Forgetting to plot wind direction on chart for angle analysis
❌ Ignoring wind-against-tide warnings
❌ Failing to check almanac for local weather effects
❌ Using outdated forecasts (>24 hours old)
❌ Not accounting for combined pressure + tide + wind effects

### Assessment Criteria

You should be able to:
- Calculate depth reduction from given pressure reading
- Evaluate forecast suitability for specific passage type
- Integrate multiple forecast sources for routing decision
- Apply almanac information to weather scenario
- Analyze wind direction effects on sea conditions
- Create weather routing plan with alternatives
- Synthesize pressure, tide, and wind effects

### Practical Application

**Scenario**: Harbor entry with charted depth 3.0m, draft 1.8m, HW-2, pressure 1025mb

1. **Predicted depth**: 3.0m + HOT (check tide tables)
2. **Pressure effect**: 1025 - 1013 = 12mb = 12cm reduction
3. **Adjusted depth**: Predicted - 0.12m
4. **Safety margin**: Ensure >0.5m under keel after adjustments
5. **Decision**: If insufficient, wait for better tide or pressure drop

**Scenario**: Planning 50nm coastal passage, southwest wind F4, ebb tide

1. **Wind direction**: Plot on chart - beam reach expected
2. **Tide effect**: Ebb opposing southwest wind = rougher sea
3. **Headlands**: Check for wind-against-tide at prominent points
4. **Timing**: Consider departure when tide turns favorable
5. **Almanac**: Check for local effects (bars, overfalls, etc.)
6. **Alternatives**: Identify ports of refuge along route

---

**Version**: 1.0.0 (v1.2.0 - 2025-11-10)
