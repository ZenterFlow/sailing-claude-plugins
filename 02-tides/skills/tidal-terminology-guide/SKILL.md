---
name: tidal-terminology-guide
description: Master tidal terminology and vertical datums (MHWS, MLWS, HAT, LAT, CD) for safe depth calculations.
license: CC-BY-SA
---

# SKILL: tidal-terminology-guide
**RYA Yachtmaster – Tidal Terminology and Vertical Datums**

## Purpose
Understand and apply tidal terminology and vertical reference planes for accurate depth and clearance calculations. Essential foundation for all tidal work.

## Activation Triggers
- "tidal terminology"
- "chart datum"
- "HAT LAT"
- "MHWS MLWS"
- "tidal range"
- "what is CD"
- "vertical datums"

## Behaviour
Explain tidal terms and their practical applications:

### Vertical Reference Planes

**Chart Datum (CD)**
- Reference plane for charted depths
- Usually set near LAT (Lowest Astronomical Tide)
- All charted depths measured BELOW Chart Datum
- Water level above CD = "height of tide"

**HAT (Highest Astronomical Tide)**
- Maximum possible tide under astronomical conditions
- Used for bridge/overhead clearances (safety-critical)
- Occurs rarely (once per 18.6 year cycle)

**LAT (Lowest Astronomical Tide)**
- Minimum possible tide under astronomical conditions
- Chart Datum usually set at or near LAT
- Provides safety margin (tide rarely falls below CD)

### Tidal Levels (Mean Values)

**Springs (Larger tides)**
- **MHWS**: Mean High Water Springs (average spring high)
- **MLWS**: Mean Low Water Springs (average spring low)

**Neaps (Smaller tides)**
- **MHWN**: Mean High Water Neaps (average neap high)
- **MLWN**: Mean Low Water Neaps (average neap low)

### Tidal Range
**Range** = High Water height - Low Water height

Example:
- HW: 5.2m above CD
- LW: 1.3m above CD
- Range: 5.2 - 1.3 = 3.9m

## Example Output
```
TIDAL TERMINOLOGY REFERENCE
═══════════════════════════════════════

VERTICAL DATUMS (Highest to Lowest)
─────────────────────────────────────

HAT (Highest Astronomical Tide)
│   ↑ Bridge clearances measured from here
│   │ (safety margin for maximum possible tide)
│
MHWS (Mean High Water Springs)
│   ↑ Average spring high water
│   │ Light elevations measured from here
│   ↑ Typical spring tidal range
│   │
MHWN (Mean High Water Neaps)
│   ↑ Average neap high water
│   │ Smaller tidal range
│   │
MSL (Mean Sea Level)
│   ~ Midpoint reference
│   │
MLWN (Mean Low Water Neaps)
│   ↓ Average neap low water
│   │
MLWS (Mean Low Water Springs)
│   ↓ Average spring low water
│
CD/LAT (Chart Datum / Lowest Astronomical Tide)
    ↓ Reference for charted depths
    │ (Tide rarely falls below this level)
    ↓

═══════════════════════════════════════

PRACTICAL APPLICATIONS
─────────────────────────────────────

1. DEPTHS
   Charted depth: 3.2m (below CD)
   Height of tide: 2.1m (above CD)
   Total depth: 3.2 + 2.1 = 5.3m ✓

2. DRYING HEIGHTS
   Chart shows: 1.5 (underlined, in brackets)
   Meaning: Rock dries 1.5m above CD
   At LW 0.8m: Rock exposed (0.8 < 1.5) ⚠️
   At HW 3.2m: Rock covered by 1.7m (3.2 - 1.5) ✓

3. BRIDGE CLEARANCES
   Chart: "Clearance 18m (HAT)"
   At MHWS (4.5m): Actual clearance ~19m
   At HAT (5.2m): Minimum clearance 18m
   → Use HAT value for safety

4. LIGHT ELEVATIONS
   Chart: "Light 23m (MHWS)"
   Measured from typical high water spring level
   Helps identify lights from distance

═══════════════════════════════════════

TERMINOLOGY QUICK REFERENCE
─────────────────────────────────────

Chart Datum (CD)
• Reference plane for charted depths
• Usually at LAT (lowest possible tide)
• Provides safety margin

Height of Tide
• Water level ABOVE Chart Datum
• Changes throughout day
• Predicted in tide tables

Tidal Range
• Difference between HW and LW
• Large range = springs
• Small range = neaps

Total Depth
• Charted depth + Height of tide
• What you actually have under keel
• Minimum = charted depth (at LAT)

Drying Height
• Height object rises ABOVE Chart Datum
• Shown underlined or in brackets on chart
• Exposed when tide height < drying height

Overhead Clearance
• Usually measured from HAT (max safety)
• Older charts may use MHWS (check notes!)
• Actual clearance = Charted clearance + (HAT - current tide height)
```

## Key Relationships

### Depth Calculation
```
Total Depth = Charted Depth + Height of Tide

Example:
Charted: 3.2m
Tide: 2.1m above CD
Total: 5.3m ✓
```

### Drying Height
```
If tide height < drying height → Rock EXPOSED
If tide height > drying height → Rock COVERED

Example:
Drying height: 1.5m
Tide: 0.8m → EXPOSED (0.8 < 1.5) ⚠️
Tide: 3.2m → Covered by 1.7m (3.2 - 1.5) ✓
```

### Overhead Clearance
```
Actual Clearance = Charted Clearance + (HAT - Current Tide Height)

Example:
Charted clearance: 18m (at HAT)
HAT: 5.2m
Current tide: 3.5m
Actual clearance: 18 + (5.2 - 3.5) = 19.7m ✓
```

## Common Errors to Avoid
- **Confusing CD with sea level** → CD is near LAT, not MSL
- **Using MHWS for clearances** → Use HAT (older charts may differ, check!)
- **Forgetting drying heights are ABOVE CD** → They're positive values
- **Adding when should subtract** → Clearance increases as tide falls
- **Not checking datum notes on chart** → Older charts may use different datums

## Memory Aids
**"HAT Above The Bridge"** - Bridge clearances from HAT
**"Lights Love Springs"** - Light elevations from MHWS
**"Chart Datum's the Deepest"** - CD near LAT, lowest level

## Version
v1.0.0 (2025-11-10)
