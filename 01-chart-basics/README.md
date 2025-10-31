# Plugin 01: Chart Basics

**RYA/ASA YachtMaster – Chart Fundamentals, Datums, Symbols & Compass**

## What This Plugin Teaches
- Geodetic datums (GPS ↔ Chart compatibility checks)
- Vertical datums (HAT, MHWS, CD, LAT, MSL)
- Chart symbols and abbreviations (INT 1 / 5011)
- Mercator projection basics
- Compass errors (variation & deviation)

## Skills Included
1. **datum-guardian** - GPS/chart datum compatibility and shift calculations
2. **charted-height-interpreter** - Vertical datum reference guide
3. **symbol-spotter** - Interactive chart symbol quiz with 100+ symbols
4. **compass-converter** - True ↔ Magnetic ↔ Compass conversions

## Agent
**Chart Basics Tutor** - Patient instructor focusing on precision and safety

## How to Use
Activate by asking chart-related questions:
- "Can I plot WGS-84 onto BA 2454?"
- "Is that lighthouse height above HAT or MHWS?"
- "Test me on chart symbols"
- "Convert 085°T to compass, variation 5°W, deviation +2°E"

## Status
✅ **Ready for Testing** - 4 skills fully implemented

## Example Session
```
User: "Can I plot WGS-84 straight onto BA 2454?"

Agent: Let me check the geodetic datum compatibility for you.

✅ SAFE TO PLOT

BA 2454 (Approaches to Portsmouth) uses WGS-84 geodetic datum.
Your GPS is also WGS-84.

→ No shift required - plot position directly as read from GPS.

Always check chart title block for datum before plotting.
```

## Version
v0.1.0 (2025-10-31)
