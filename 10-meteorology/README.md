# Plugin 10: Meteorology

**Status**: ✅ Complete (6 skills implemented)

The Meteorology Tutor teaches comprehensive weather forecasting, pressure systems, cloud identification, local effects, and practical weather routing for safe navigation decisions.

## Skills (6 total)

### Fundamentals (1 skill)
1. **meteorology-fundamentals** - Weather information sources, shipping forecast, GRIB files, forecast evaluation, data logging

### Global Systems (2 skills)
2. **global-weather-systems** - Pressure patterns, Coriolis effect, Buys Ballot's Law, trade winds, sea state vs swell
3. **weather-interactions** - System interactions, frontal passages, depression lifecycle, squeeze zones, barometric monitoring

### Practical Forecasting (2 skills)
4. **cloud-types** - Cloud identification, cloud sequences, cumulonimbus hazards, visibility prediction
5. **local-weather-fog** - Sea breezes, katabatic/anabatic winds, fog types, fog navigation procedures

### Applied Navigation (1 skill)
6. **pressure-forecast-application** - Pressure effects on depth, weather routing, wind-against-tide, almanac integration

## Installation

```bash
/plugin install meteorology@sailing-curriculum
```

## Usage Examples

### Forecast Selection
```
User: Planning 3-day offshore passage. What forecast sources should I use?

Agent: OFFSHORE PASSAGE FORECAST STRATEGY

       Primary: Synoptic charts (3-5 day system movement)
       Supplementary: GRIB files (wind/wave trends)
       Validation: Shipping forecast (current conditions)
       Local: Inshore forecast (departure/arrival harbors)
       Live: ODAS buoy observations (actual conditions)

       Cross-reference all sources, check issue time (<24hrs).
```

### Pressure Systems
```
User: Wind from south, Northern Hemisphere. Where is low pressure?

Agent: BUYS BALLOT'S LAW (NH)

       "Back to blow, left to low"

       Wind from south → Face south (back to wind)
       Low pressure is on your LEFT (east)

       Circulation: Anticlockwise around low
       Expect: Wind to veer (clockwise) as system passes
```

### Cloud Identification
```
User: High wispy clouds appearing. What does this mean?

Agent: CIRRUS CLOUDS - FRONTAL SYSTEM APPROACHING

       Type: High altitude, wispy/feathery
       Timeframe: 12-24 hours to system arrival

       Expected sequence:
       1. Cirrus (now)
       2. Cirrostratus (halo around sun/moon)
       3. Altostratus (sun through frosted glass)
       4. Nimbostratus (continuous rain)

       Action: Monitor barometer, prepare for frontal passage
```

### Sea Breeze
```
User: Sunny day, light offshore wind. Planning afternoon sail?

Agent: SEA BREEZE CONDITIONS

       Expect: Sea breeze will develop mid-day
       Peak: Mid-afternoon
       Strength: Force 3-4 (enhanced by offshore wind)

       Route planning:
       • Morning: Offshore wind
       • Afternoon: Beam reach with sea breeze
       • Evening: Wind dies as land cools

       Benefit: Inshore waters smoother (short fetch)
```

### Fog Navigation
```
User: Just encountered fog bank. What should I do?

Agent: FOG NAVIGATION - IMMEDIATE ACTIONS

       1. Life jackets: All crew don life jackets
       2. Position: Fix EP from last known position
       3. Lights: Display navigation lights
       4. Sound signals: 1 long + 2 short every 2 min (sailing)
       5. Speed: Reduce to safe speed
       6. Lookout: Post additional crew, wake sleeping
       7. Radar: Activate radar and reflector

       Navigation: Use depth sounder, follow safe contours
       Traffic: Head away from shipping channels
```

### Pressure Effect on Depth
```
User: Harbor entry depth 3.0m charted, draft 1.8m, pressure 1025mb. Safe?

Agent: PRESSURE EFFECT CALCULATION

       Standard pressure: 1013mb
       Current pressure: 1025mb
       Difference: +12mb

       Depth reduction: 12mb × 1cm/mb = 12cm less depth

       Actual depth: 3.0m + HOT - 0.12m
       Required: 1.8m draft + 0.5m safety = 2.3m minimum

       Decision: Check HOT value. If insufficient clearance,
                wait for pressure drop or better tide.
```

## Topics Covered

### Weather Information Sources
- Shipping forecast (marine radio, NAVTEX, internet, format, validity)
- Inshore waters forecast (local effects, coastal coverage)
- Maritime Safety Information (MSI) broadcasts
- Synoptic/surface pressure charts (system tracking, 3-5 day planning)
- Computer models (GFS, ECMWF)
- GRIB files (format, access, resolution, limitations)
- Live observations (ODAS buoys, ship reports, weather stations)
- Forecast evaluation (6-criteria checklist)

### Global Weather Systems
- Atmospheric convection and lapse rate (6.5°C per 1,000m)
- High and low pressure characteristics
- Coriolis effect (maximum at poles, minimum at equator)
- Buys Ballot's Law (both hemispheres)
- Pressure gradient and wind strength (isobar spacing)
- Global pressure bands (ITCZ, doldrums, subtropical high, subpolar low)
- Geostrophic vs surface wind (2/3 speed, backed 15°)
- Sea state vs swell (local vs distant waves)

### System Interactions
- High-high, high-low, low-low interactions
- Squeeze zones (strongest winds between systems)
- Depression lifecycle (formation, wave, mature stages)
- Frontal passages (warm front, warm sector, cold front sequences)
- Barometric monitoring (>6mb/3hr = F6, >8mb/3hr = F8)
- System speed definitions (slowly to very rapidly)

### Cloud Identification
- Cloud shapes (flat = stable, puffy = unstable)
- Low clouds (stratus, cumulus, nimbostratus, fractostratus)
- Medium clouds (altostratus, altocumulus)
- High clouds (cirrus, cirrostratus, cirrocumulus)
- Cumulonimbus (multi-level, 12km height, thunderstorm hazards)
- Frontal cloud sequences
- Weather prediction from cloud patterns
- Visibility changes with cloud types

### Local Weather Effects
- Sea breeze formation (process, timing, Force 4 max)
- Land breeze (nighttime, weaker than sea breeze)
- Katabatic winds (gravity-driven, sudden, violent)
- Anabatic winds (upslope, daytime)
- Radiation fog (land, winter, cold clear nights)
- Advection fog (sea, spring/summer, warm air over cold sea)
- Fog navigation (7-step immediate actions, contour navigation)
- Wind direction fundamentals (from not to, backing, veering)
- Wind-topography interactions (convergence, divergence)
- Onshore vs offshore wind effects

### Applied Meteorology
- Pressure effects on depth (1mb = 1cm)
- Forecast source selection by passage type
- Weather routing (port selection, alternatives, timing)
- Wind direction analysis relative to route
- Sea state factors (fetch, depth proximity, wind-against-tide)
- Almanac integration (local effects, bar warnings, exposure)
- Forecast validation checklist

## Version
v1.2.0 (2025-11-10)
