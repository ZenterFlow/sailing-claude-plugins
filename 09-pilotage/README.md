# Plugin 09: Pilotage

**Status**: ✅ Ready for Testing (6 skills implemented)

The Pilotage Tutor teaches safe harbor approaches, clearing bearings, leading lines, and navigation in restricted visibility.

## Skills (6 total)

1. **chart-update-checker** - Verify charts are current and legal (SOLAS V requirement)
2. **almanac-navigator** - Harbor entry notes and pilotage directions
3. **clearing-bearing-calculator** - Calculate NMT/NLT danger bearings for hazard avoidance
4. **leading-line-plotter** - Leading lines and transits for accurate position fixing
5. **harbor-entry-planner** - Comprehensive harbor approach plans with abort criteria
6. **restricted-visibility-navigator** - Fog procedures and COLREGS sound signals

## Installation

```bash
/plugin install pilotage@sailing-curriculum
```

## Usage Examples

### Clearing Bearing
```
User: Rock at 50°20'N 004°10'W. Passing north. Reference is lighthouse at 50°22'N 004°08'W. What clearing bearing?

Agent: Calculates bearing from rock to lighthouse (028°T).
       Safe water is north (left of line).
       Rule: Keep lighthouse bearing NMT 028°T
       Provides monitoring guidance and magnetic conversion.
```

### Harbor Entry Plan
```
User: Create entry plan for Dartmouth. Draught 1.8m, SW F4, HW-2.

Agent: Complete plan with:
       - Approach track and clearing bearings
       - Entry procedures and leading lines
       - Abort criteria (wind, depth, navigation)
       - Plans A, B, C
       - Crew briefing points
```

### Restricted Visibility
```
User: Visibility dropped to 0.5nm. We're sailing. What do I do?

Agent: Immediate actions:
       - Reduce speed to safe speed
       - Sound signal: 1 long + 2 short every 2 min
       - Post lookout, lights on
       - Monitor radar/VHF
       - Provides full fog procedures checklist
```

## Topics Covered

- Pilotage planning and preparation
- Leading lines and transits
- Clearing bearings (NMT/NLT danger bearings)
- Depth contour navigation
- Harbor entry procedures with abort criteria
- Restricted visibility navigation (COLREGS Rule 19)
- Sound signals (COLREGS Rule 35)
- Traffic separation schemes
- Port entry protocols

## Version
v0.2.0 (2025-11-09)
