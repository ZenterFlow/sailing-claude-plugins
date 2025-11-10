# Plugin 03: Positioning

**Status**: ✅ Complete (8 skills implemented)

The Positioning Tutor teaches position fixing, estimated position (EP), dead reckoning (DR), cross-track error monitoring, and specialized navigation techniques.

## Skills (8 total)

### Core Position Fixing
1. **visual-fix-calculator** - Three-point fixes, running fixes, cocked hat assessment
2. **ep-calculator** - Estimated Position and Dead Reckoning with leeway and tidal stream
3. **cross-track-error-monitor** - XTE calculation and monitoring for TSS and channels

### Advanced Techniques
4. **visual-fix-reliability** - Assess visual fix quality and reliability using cocked hat analysis
5. **enhanced-visual-fixing** - Advanced visual fixing techniques (running fixes, four-point fixes)
6. **position-fix-integrator** - Complete position fixing workflow integration

### Specialized Methods
7. **navigation-web-constructor** - Pre-plotted bearing/distance grids for rapid GPS monitoring and tacking decisions
8. **angle-off-bow-fix** - Quick distance-off estimation using 45°/90° relative bearing method

## Installation

```bash
/plugin install positioning@sailing-curriculum
```

## Usage Examples

### Visual Position Fix
```
User: I have bearings: North Head 045°C, South Light 110°C, East Point 160°C.
      Deviation 2°W, Variation 5°E. What's my position?

Agent: Converts bearings to true, plots reciprocals, assesses cocked hat,
       provides position with quality rating.
```

### Estimated Position
```
User: Last fix at 09:00 was 50°30'N 002°00'W. Steering 090°C at 5 knots.
      Now 11:00. Wind SW, leeway 7°. Stream 135°T at 1.5 kts. What's my EP?

Agent: Calculates DR, applies leeway, applies stream, provides EP with
       confidence assessment.
```

### Cross-Track Error
```
User: In Dover Strait TSS northbound. Track 045°T from 51°00'N 001°25'E.
      Now at 51°08'N 001°38'E. Am I safe?

Agent: Calculates XTE, assesses against lane width, provides safety status
       and correction recommendations.
```

## Topics Covered

- Visual position fixing (compass bearings, ranges, transits)
- Three-point fix and running fix
- Estimated Position (EP) with leeway and tidal stream
- Dead Reckoning (DR) from course and speed
- Circle of error and fix accuracy
- Cross-track error (XTE)
- GPS position validation
- Position line advancement

## Version
v0.4.0 (2025-11-10)
