# SKILL: Atmospheric Pressure Effects and Forecast Application (SKILL_90)

## Description
Apply atmospheric pressure effects on tidal heights, interpret weather forecasts for navigation decisions, and synthesize multiple data sources for route planning.

## Prerequisites
- Local Weather Effects (SKILL_89)

## Learning Objectives
- Calculate pressure effects on water depth
- Evaluate forecast suitability for navigation decisions
- Apply weather information to routing decisions
- Interpret wind effects on sea conditions
- Synthesize multiple forecast sources

**Pressure Effects on Water Depth**

**Standard Pressure:**
- **UK Standard:** 1013mb (assumed pressure for tide tables)
- **Global Reference:** Average sea level pressure

**Pressure-Depth Relationship:**
- **General Rule:** 1mb above standard = 1cm less water depth
- **Example Calculation:**
  - Pressure: 1035mb
  - Difference: 1035 - 1013 = 22mb
  - Depth Reduction: 22cm less than predicted
- **Critical Thresholds:**
  - &gt;10mb above standard: Significant consideration needed
  - Critical depth situations: Even 5-10cm can matter
- **Low Pressure:** Below 1013mb = deeper water than predicted

**Practical Implications:**
- **Harbor Entry:** High pressure could reduce depth below safe limit
- **Bridge Clearance:** Low pressure increases air draft clearance (usually less critical)
- **Combined Factors:** Pressure is one of many factors - combine with:
  - Tidal state (height of tide)
  - Wind direction and strength
  - Wave/swell conditions

**Forecast Interpretation for Navigation**

**Forecast Sources and Uses:**

**Synoptic Charts:**
- **Scale:** Large area (thousands of miles)
- **Best For:** Medium to long-term planning (3-5+ days)
- **Limitation:** Needs refinement for local sailing
- **Information:** System positions, movement, pressure gradients

**Shipping Forecast:**
- **Scale:** Sea area (regional)
- **Best For:** Short to medium-term planning, offshore passages
- **Validity:** 24 hours typically
- **Information:** Wind, weather, visibility, pressure tendency

**Inshore Waters Forecast:**
- **Scale:** Fixed coastline stretches
- **Best For:** Short-term, local passages
- **Advantage:** Includes local effects
- **Information:** Detailed coastal conditions

**GRIB Files:**
- **Scale:** Varies (100km+ for free versions)
- **Best For:** Long-term offshore planning, trend analysis
- **Limitation:** Not suitable for short-term local decisions
- **Information:** Wind, rain, pressure, wave data

**Mobile App Forecasts (GFS-based):**
- **Scale:** Regional to local
- **Best For:** Supplementing official forecasts
- **Format:** 3-hour blocks (conditions change gradually)
- **Information:** Multiple parameters (wind, rain, temperature)

**Live Observations:**
- **Sources:** ODAS buoys, weather stations, ship reports
- **Best For:** Real-time verification of forecasts
- **Use:** Update synoptic information, confirm conditions

**Weather Routing Applications**

**Primary Use:** Determine if conditions suitable for vessel and crew

**Specific Applications:**
1. **Port Selection:** Best shelter for given conditions
2. **Alternative Havens:** Identify ports of refuge
3. **Route Adjustment:** Modify planned route for weather
4. **Departure Timing:** Choose favorable weather window
5. **Tide-Wind Interaction:** Avoid wind-against-tide conditions

**Wind Direction Analysis**
Plot wind direction on chart to determine angle relative to vessel:
- **Windward (Beat):** Slowest, most challenging
- **Beam Reach:** Fastest, comfortable sailing
- **Dead Run:** Risk of rolling, seasickness

**Sea State Factors**

**Components Affecting Sea Conditions:**
1. **Wind Direction vs Tide Direction:**
   - Same direction = calmer sea
   - Opposite direction = rougher sea
2. **Fetch:** Distance wind travels over water
   - Longer fetch = larger wave height
3. **Depth Proximity:**
   - Offshore wind near shore = calmer
   - Onshore wind near shore = breaking waves, dangerous
4. **Wind-Against-Tide:**
   - Can cause serious seas even in moderate conditions
   - Avoid rounding headlands in these conditions

**Almanac Integration Example**
**Sweetwater Bay Question:** After prolonged strong westerly winds, what sea conditions at bar entrance near LW?

**Analysis Process:**
1. **Consult Almanac:** Page 77 for Sweetwater information
2. **Key Information:** Bar "dangerous at LW with westerly swell"
3. **Specific Warning:** "2m swell offshore generates dangerous breaking swell on bar; do not attempt entry"
4. **Conclusion:** Anchorage "untenable" in westerly swell
5. **Alternative:** Consider Jackson Bay to north
6. **Further Check:** Jackson Bay open to NW - if wind veers, becomes unsafe
7. **Final Decision:** Need alternative destination based on forecast wind direction

**Forecast Validation Checklist**
1. **Coverage:** Does forecast cover sailing area?
2. **Timeliness:** Issued within last 24 hours?
3. **Scale:** Appropriate for passage type?
4. **Completeness:** All required parameters included?
5. **Cross-Reference:** Multiple sources available?
6. **Local Knowledge:** Consult almanac for area-specific effects

**Almanac Information Types:**
- Sea areas and forecast regions (page 3 example)
- Live observations from ODAS buoys (page 4)
- Shipping forecast schedule and content (page 5)
- Inshore forecast areas (page 4)
- Synoptic chart timing (analysis vs forecast)
- Local port/harbor weather sensitivities
- Specific hazard warnings (bars, overfalls, etc.)

## Common Errors
- Not considering pressure effects on critical depths
- Using non-marine forecasts for navigation decisions
- Relying on single forecast source without validation
- Forgetting to plot wind direction on chart for angle analysis
- Ignoring wind-against-tide warnings
- Failing to check almanac for local weather effects
- Using outdated forecasts (&gt;24 hours old)

## Assessment
- Calculate depth reduction from given pressure reading
- Evaluate forecast suitability for specific passage type
- Integrate multiple forecast sources for routing decision
- Apply almanac information to weather scenario
- Analyze wind direction effects on sea conditions
- Create weather routing plan with alternatives

***