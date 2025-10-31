# Plugin 02: Tides

**RYA/ASA YachtMaster – Complete Tidal Calculations Suite**

## What This Plugin Teaches
- Tidal height calculations (primary & secondary ports)
- Tidal curves and rule-of-twelfths
- Tidal stream predictions and tidal diamonds
- Depth safety and under-keel clearance
- Vertical clearance calculations (bridges)
- Drying height conversions

## Skills Included
1. **tide-calculator** - Tidal height/time calculations using curves and twelfths
2. **tidal-diamond-reader** - Full diamond table display (HW-3 to HW+3)
3. **diamond-dispatcher** - Quick diamond lookup for specific hours
4. **depth-datum-flipper** - Depth safety calculations, drying heights, UKC checks
5. **vertical-clearance-solver** - Bridge/wire clearance calculations

## Agent
**Tides Tutor** - Methodical, safety-focused, shows all workings

## How to Use
Activate by asking tidal questions:
- "What's the tide at Portsmouth at 14:30 on June 15?"
- "Diamond F at HW+3, spring tides"
- "Draught 1.8m, chart shows 3.2m, tide 2.1m - am I safe?"
- "Bridge 22m above HAT, tide +1.2m, mast 19.5m"
- "Drying 1.2m, tide 2.5m, can I pass?"

## Status
✅ **Ready for Testing** - 5 skills fully implemented

## Example Session
```
User: "Drying 1.2m, tide 2.5m, draught 1.5m, need 0.5m UKC"

Agent: Drying height - let's calculate carefully!

Water Depth = Tide - Drying Height
            = 2.5m - 1.2m
            = 1.3m

Required: 1.5m + 0.5m = 2.0m

⚠️ INSUFFICIENT DEPTH - GROUNDING RISK

Shortfall: 0.7m
Wait until tide reaches at least 2.7m CD
```

## Version
v0.1.0 (2025-10-31)
