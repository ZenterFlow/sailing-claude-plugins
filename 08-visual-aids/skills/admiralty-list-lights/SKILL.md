# Admiralty List of Lights and Navigation Data

---
name: admiralty-list-lights
version: 1.0.0
triggers:
  - "admiralty list"
  - "list of lights"
  - "notices to mariners"
  - "light publication"
  - "sector lights"
  - "moire lights"
  - "light almanac"
---

## Purpose

Locate, interpret, and maintain information from the Admiralty List of Lights and other navigation publications for safe passage planning and execution.

## Activation Triggers

This skill activates when you ask about:
- Admiralty List of Lights usage
- Navigation publication interpretation
- Updating light information
- Sector lights or moire lights
- Alternative light information sources

## Behavior

### Admiralty List of Lights Overview

**What It Is**: Comprehensive worldwide reference for navigation lights in multiple volumes, available in hard copy and digital format

**Detail Level**: More detailed than almanacs - official source for light characteristics

**Purpose**: Provides complete, authoritative information for passage planning

### Key Information Per Light Entry

Each light entry contains:

**1. Reference Number**: Unique identifier for the light

**2. Name and Location**: Official name and geographic position description

**3. Position**: Latitude/Longitude coordinates (degrees, minutes, seconds)

**4. Characteristic**: Light sequence pattern
- Example: Fl(3)WRG.10s
- Format: [Type]([Group])[Color].[Period]
- Decodes to: Group flashing (3) White/Red/Green every 10 seconds

**5. Height**: Height of light above chart datum (meters)
- Critical for dipping distance calculations
- Add tide height for actual height

**6. Range**: Nominal range in nautical miles
- Standardized for 10nm visibility
- Multiple ranges may indicate sector lights

**7. Structure**: Physical description
- Tower, building, post, etc.
- Helps with visual identification
- Color and markings noted

**8. Remarks**: Additional critical information
- Fog signals (type and range)
- Radar beacons (RACON)
- Operational notes
- Seasonal variations

### Information Formats

**Hard Copy**:
- Traditional book format in multiple volumes
- Requires manual updates via Notices to Mariners
- Portable, no power required
- Regional volumes (e.g., Volume A: British Isles)

**Digital Format**:
- Electronic versions with search capability
- Can be updated electronically
- Integrated with chart plotting software
- Searchable by name, position, or characteristic

**Coverage**: Worldwide in multiple geographical volumes

### Updates and Corrections

**Method**: Through Notices to Mariners (weekly publications)

**Process**:
1. Check weekly Notices to Mariners
2. Hand-correct hard copies OR update digital versions
3. Note changes on relevant charts
4. File corrections chronologically

**Importance**: Light characteristics can change temporarily (maintenance) or permanently (upgrades)

**Critical Changes**:
- Light extinguished
- Characteristic changed
- Position altered
- Range modified
- Fog signal added/removed

### Alternative Light Information Sources

**RYA Training Almanac**:
- Contains key lights for training areas
- Simplified format for students
- Updated annually

**Reeds Nautical Almanac**:
- Popular cruising reference
- Covers UK, Channel, North Sea, Med
- Includes lights, tides, harbors
- Annual publication

**Local/Regional Almanacs**:
- May have detailed regional information
- Often include pilotage notes
- Examples: Solent Guide, Channel Pilot

**Chart Information Boxes**:
- Special marks and local notes
- Quick reference for specific area
- Cross-reference with List of Lights

### Electronic Charts Considerations

**Appearance**: May differ between paper and electronic charts

**Consistency**:
- Shapes should be similar across formats
- Colors remain the same if shown
- Symbols standardized (but rendering varies)

**Light Sequences**: Remain identical across all formats

**Example**: BYB (Black-Yellow-Black) easterly cardinal has same light sequence regardless of chart type

### Supplementary Light Information

**Sector Lights**:
- Show safe passage sectors with color transitions
- Example: White sector = safe water, Red sector = danger
- Multiple ranges indicate different sectors
- Example entry: "15M W, 12M R, 10M G"

**Leading Lights/Range Lights**:
- Two lights in transit mark safe channel
- Front light lower than rear light
- Keep aligned for safe passage

**Moire Lights** (Bridge Clearance):
- Visible only from certain angles
- Used on bridges for alignment indication
- Goes out or changes color if vessel strays off course
- Critical for narrow channel navigation

**Fog Signals**:
- Detailed in Remarks column
- Type: Horn, Siren, Bell, Whistle
- Pattern: Morse, number of blasts
- Example: "Horn(2)30s" = 2 blasts every 30 seconds

### Practical Use Workflow

**1. Passage Planning**:
- Extract range, height, and characteristic for all critical lights
- Note fog signal details
- Identify RACON-equipped marks
- Plan position fix opportunities

**2. Position Fixing**:
- Use light characteristics to verify identity when sighted
- Confirm bearing matches expected
- Check light color matches sector

**3. Range Prediction**:
- Check nominal range vs expected visibility conditions
- Calculate geographical range for your height of eye
- Adjust expectations for weather

**4. Updates**:
- Verify latest corrections before voyage
- Check Temporary and Preliminary Notices
- Update personal copies or digital versions

### Example Light Entry Interpretation

**Entry**:
```
Point Victoria LH
50°42'.3N 001°15'.8W
Fl(4)WRG.15s  20m  24M W, 20M R, 18M G
White tower, red bands
Racon(T)
Horn(2)60s
```

**Interpretation**:
- **Location**: Point Victoria Lighthouse at 50°42'.3N 001°15'.8W
- **Characteristic**: Group flashing 4, white/red/green, every 15 seconds
- **Height**: 20 meters above chart datum
- **Range**: Sector light - 24M white sector, 20M red, 18M green
- **Structure**: White tower with red bands (daymark)
- **RACON**: Morse "T" on radar
- **Fog Signal**: Horn, 2 blasts every 60 seconds

### Common Errors to Avoid

❌ Using outdated light information without checking Notices to Mariners
❌ Confusing nominal range with guaranteed visibility distance
❌ Overlooking Remarks column for critical fog signal information
❌ Assuming all light lists have same detail level as Admiralty
❌ Not cross-referencing chart information boxes
❌ Ignoring sector light color transitions
❌ Forgetting to add tide height to light height

### Assessment Criteria

You should be able to:
- Extract all key data from sample light entry
- Describe correction procedures for light changes
- Compare information depth across different sources
- Apply light data to passage planning scenario
- Identify critical information in Remarks column
- Interpret sector light ranges correctly

### Practical Application

**Scenario**: Planning night approach to harbor, checking light details

1. **Look up harbor entrance light** in List of Lights
2. **Extract data**: Fl.3s 15m 12M, Horn(1)30s, Racon(M)
3. **Calculate range**: 2.08√3 + 2.08√15 = 11.7nm (your height of eye 3m)
4. **Expect visibility**: Light should appear at ~11-12nm
5. **Fog preparation**: Note horn signal (1 blast per 30s)
6. **Radar**: Look for Morse "M" if using radar approach

**Scenario**: Light characteristic doesn't match chart

1. **Check Notice to Mariners** for recent changes
2. **Verify position** - ensure you're looking at correct light
3. **Consider** temporary extinguishment or maintenance
4. **If critical**: Report discrepancy to authorities
5. **Navigate**: Use alternative position fixing methods

---

**Version**: 1.0.0 (v1.0.0 - 2025-11-10)
