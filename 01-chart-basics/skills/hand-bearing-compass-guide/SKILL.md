---
name: hand-bearing-compass-guide
description: Take accurate hand bearing compass readings for position fixing and collision avoidance while minimizing magnetic interference.
license: CC-BY-SA
---

# SKILL: hand-bearing-compass-guide
**RYA Yachtmaster – Hand Bearing Compass Techniques**

## Purpose
Take accurate magnetic bearings using a hand bearing compass for position fixing (cross bearings) and collision avoidance (steady bearing = collision risk). Minimize magnetic interference and apply proper technique.

## Activation Triggers
- "hand bearing compass"
- "take a bearing"
- "position fix"
- "cross bearing"
- "collision avoidance"
- "steady bearing"
- "three point fix"

## Behaviour
Teach proper hand bearing compass technique:

### Position Fixing (Cross Bearings)
1. Select 2-3 conspicuous charted objects (lighthouses, headlands, towers)
2. Take bearings quickly in sequence (<2 minutes total)
3. Record each bearing: object name + bearing(M)
4. Plot on chart from objects seaward
5. Intersection = vessel position

### Collision Avoidance
- Take bearing of approaching vessel
- Wait 3-5 minutes, take bearing again
- **Steady bearing = collision risk** (constant bearing, decreasing range)
- **Changing bearing = safe passage** (bearing opening or closing)

### Minimizing Magnetic Interference
**Critical**: Hand bearing compass has NO deviation table
- Stand AWAY from metal, electronics, speakers, engine
- Minimum 1-2m from large metal objects
- Hold at arm's length when possible
- Check for interference by rotating 360° at same spot
- Keep compass level and steady

## Example Output
```
HAND BEARING COMPASS - POSITION FIX
═══════════════════════════════════════

TECHNIQUE:
1. Select 3 conspicuous charted objects
2. Take bearings in quick succession (<2 min)
3. Apply variation only (NO deviation)
4. Plot from objects seaward

BEARINGS TAKEN (14:23 UTC):
─────────────────────────────────────
Object 1: St Catherine's Lighthouse
Bearing: 045°M

Object 2: Needles Lighthouse
Bearing: 315°M

Object 3: Nab Tower
Bearing: 072°M

VARIATION: 3°W (from chart)

CONVERSION TO TRUE:
─────────────────────────────────────
St Catherine's: 045°M - 3°W = 042°T
Needles: 315°M - 3°W = 312°T
Nab Tower: 072°M - 3°W = 069°T

PLOT ON CHART:
─────────────────────────────────────
From St Catherine's: plot 042°T seaward
From Needles: plot 312°T seaward
From Nab Tower: plot 069°T seaward

Intersection = Vessel Position ⊙

COCKED HAT:
Size: ~200m (acceptable for coastal)
Use center or nearest danger

QUALITY: GOOD
✓ 3 bearings (redundancy)
✓ ~60° spread (good geometry)
✓ Small cocked hat (<0.2nm)
✓ Quick succession (<2 min)
```

```
COLLISION AVOIDANCE CHECK
═══════════════════════════════════════

TARGET: Vessel approaching from port bow

TIME     BEARING    RANGE    ASSESSMENT
14:10    320°M      3.0nm    Initial
14:15    320°M      2.2nm    ⚠️ STEADY BEARING
14:20    320°M      1.5nm    🚨 COLLISION RISK

ANALYSIS:
─────────────────────────────────────
Bearing: CONSTANT at 320°M
Range: DECREASING (3.0 → 1.5nm in 10 min)
Conclusion: COLLISION RISK EXISTS

ACTION REQUIRED:
• Alter course substantially (>30°)
• Alter early and obviously
• Monitor for bearing change
• Consider IRPCS rules (give-way vessel?)

VERIFICATION:
Take new bearing after altering:
- If bearing changes: risk reduced ✓
- If bearing still steady: alter more
```

## Best Practices

### Selecting Objects for Position Fixing
**Good choices**:
- Lighthouses, headlands, prominent towers
- Charted features with clear symbols
- Objects spread ~60-90° apart (ideal geometry)

**Avoid**:
- Small buoys (poor accuracy)
- Similar objects (identification confusion)
- Objects in line (poor geometry, no fix)

### Timing
- Take all bearings in <2 minutes (vessel moving)
- Note exact time for log
- Fastest changing bearing first (ahead/astern)
- Slowest changing bearing last (abeam)

### Accuracy
- Hold steady, let compass settle
- Read to nearest 2-5° (realistic precision)
- Repeat if doubtful
- Check for magnetic interference (rotate, check consistency)

### Magnetic Interference Sources
**Strong interference** (>1m away):
- Engine block, steering gear
- Speakers, electronics
- Steel tools, cans
- Jackstays, wire rigging

**Medium interference** (>0.5m):
- Winches, fittings
- Canned food, batteries
- Mobile phones

## Common Errors to Avoid
- Standing too close to metal (most common error)
- Not taking bearings quickly enough (vessel drifting)
- Applying ship's deviation table (WRONG - portable compass)
- Using for precise navigation (should be backup to GPS)
- Forgetting to apply variation (bearings are magnetic)
- Poor object selection (buoys, distant objects)

## Position Fix Quality Assessment
- **EXCELLENT**: 3+ bearings, 60-90° spread, cocked hat <100m
- **GOOD**: 3 bearings, reasonable spread, cocked hat <200m
- **ACCEPTABLE**: 2-3 bearings, cocked hat <0.5nm
- **POOR**: 2 bearings only, poor spread, large cocked hat

## Version
v1.0.0 (2025-11-10)
