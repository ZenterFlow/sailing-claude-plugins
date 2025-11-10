# Plugin 08: Visual Aids

**Status**: ✅ Complete (11 skills implemented)

The Visual Aids Tutor teaches comprehensive recognition of buoys, lights, cardinal marks, ranges, transits, and navigation publications for safe visual navigation.

## Skills (11 total)

### Foundation (2 skills)
1. **iala-buoyage-system** - IALA Region A/B fundamentals, direction of buoyage, five mark categories
2. **lateral-marks-identifier** - Port and starboard marks with regional color variations and preferred channel indicators

### Cardinal and Special Marks (2 skills)
3. **cardinal-marks-identifier** - Identify cardinal marks (N/E/S/W) by topmarks, colors, and lights
4. **special-purpose-marks** - Isolated danger, safe water, special marks, and wreck markers

### Light Navigation (3 skills)
5. **light-characteristics-quiz** - Interactive quiz for navigation light characteristics (Fl, Oc, Iso, Q, VQ)
6. **light-ranges-beacons** - Calculate geographical/luminous/nominal ranges, dipping distance, identify RACON
7. **admiralty-list-lights** - Extract and interpret Admiralty List of Lights and navigation publications

### Visual Position Fixing (2 skills)
8. **ranges-and-transits-guide** - Visual ranges and transits for accurate position fixing
9. **dipping-distance-calculator** - Geographic range calculations for lights and objects

### Comprehensive Assessment (2 skills)
10. **direction-of-buoyage-reminder** - Quick reference for IALA buoyage rules
11. **visual-aids-quiz** - Rapid identification quiz covering all navigation marks

## Installation

```bash
/plugin install visual-aids@sailing-curriculum
```

## Usage Examples

### IALA Buoyage System
```
User: What's the difference between IALA A and B?

Agent: IALA REGIONS - LATERAL MARK COLORS

       IALA Region A (Europe, Australia):
       • RED to PORT (left)
       • GREEN to STARBOARD (right)

       IALA Region B (Americas, Asia):
       • GREEN to PORT (left)
       • RED to STARBOARD (right)

       CRITICAL: Only lateral mark colors change.
       All other marks (cardinal, isolated danger, safe water, special) are IDENTICAL worldwide.
```

### Special Purpose Marks
```
User: Black body with red horizontal band, two balls on top?

Agent: ISOLATED DANGER MARK
       • Hazard directly beneath mark
       • Navigable water all around
       • Light: Fl(2) white (2 flashes)
       • Action: Keep well clear, pass with adequate distance
```

### Light Ranges
```
User: Calculate when I'll see a 30m lighthouse. My height of eye is 4m.

Agent: GEOGRAPHICAL RANGE CALCULATION

       Distance = 2.08√4 + 2.08√30
       Distance = 4.2nm + 11.4nm = 15.6nm

       Light should appear at 15.6nm (clear weather).

       Note: This is geographical range. Actual visibility may be
       limited by weather (luminous range) or nominal range listed on chart.
```

### Admiralty List of Lights
```
User: What information is in the Admiralty List of Lights?

Agent: ADMIRALTY LIST OF LIGHTS ENTRIES

       Each light entry contains:
       • Reference number (unique ID)
       • Position (lat/long)
       • Characteristic (e.g., Fl(3)WRG.10s)
       • Height (above chart datum)
       • Range (nominal, in nautical miles)
       • Structure (tower, building, etc.)
       • Remarks (fog signals, RACON, etc.)

       Updated via Notices to Mariners (weekly).
```

## Topics Covered

### Buoyage Systems
- IALA A/B regional differences
- Direction of buoyage concept
- Five core mark categories (lateral, cardinal, isolated danger, safe water, special)

### Mark Types
- Lateral marks with regional color variations
- Preferred channel indicators (2+1 light pattern)
- Cardinal marks (N/E/S/W) with topmark recognition
- Isolated danger marks (black/red bands, two balls)
- Safe water marks (red/white vertical stripes)
- Special marks (yellow with X topmark)
- Temporary wreck markers (blue/yellow stripes)

### Light Navigation
- Light characteristics (Fl, Oc, Iso, Q, VQ, UQ, LFl, Morse)
- Geographical range (line of sight/curvature)
- Luminous range (intensity and weather)
- Nominal range (standardized for 10nm visibility)
- Dipping distance calculations (2.08√h formula)
- Sector lights and moire lights
- RACON identification on radar

### Navigation Publications
- Admiralty List of Lights usage
- Notices to Mariners corrections
- Alternative sources (Reeds, RYA almanacs)
- Chart information boxes

### Position Fixing
- Ranges and transits
- Leading lines and lights
- Light bearing fixes
- Dipping distance position lines

## Version
v1.0.0 (2025-11-10)
