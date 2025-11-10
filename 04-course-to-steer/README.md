# Plugin 04: Course to Steer

**Status**: ✅ Ready for Testing (7 skills implemented)

The Course to Steer Tutor teaches CTS calculations incorporating leeway, tidal stream, velocity triangles, and magnetic corrections.

## Skills (7 total)

### Core Calculations
1. **cts-calculator** - Course To Steer calculations with leeway, stream, and magnetic corrections
2. **velocity-triangle-plotter** - Graphical velocity triangle solutions for CTS and TMG problems

### Advanced Techniques
3. **vector-triangle-plotter** - Complete CTS vector triangle plotting on chart
4. **leeway-applicator** - Apply leeway correction to True CTS (port/starboard tack rules)
5. **multi-factor-converter** - Complete T→M→C conversion sequence with variation and deviation
6. **tidal-hour-selector** - Determine correct tidal hour for CTS based on trip timing
7. **cts-practical-integrator** - Complete end-to-end CTS workflow integration

## Installation

```bash
/plugin install course-to-steer@sailing-curriculum
```

## Usage Examples

### Calculate Course To Steer
```
User: I want to make good 090°T. Boat speed 5 knots. Stream 180°T at 2 knots.
      Wind from North, leeway 6°. Variation 5°W, deviation 2°W.
      What course do I steer?

Agent: Applies stream correction, leeway, variation/deviation.
       Provides: Steer 050°C to make good 090°T
       Includes SOG and ETA calculations.
```

### Velocity Triangle
```
User: Show me the velocity triangle for: desired track 000°T,
      boat speed 6 kts, stream 090°T at 2 kts.

Agent: Draws ASCII vector diagram showing heading, water track,
       tidal stream, and track made good with all measurements.
```

## Topics Covered

- Course to Steer (CTS) calculations
- Leeway application (typically 5-10° downwind)
- Tidal stream vectors
- Velocity triangles (water triangle)
- Magnetic variation corrections
- Track made good vs course steered
- Speed over ground calculations
- Vector navigation

## Version
v0.3.0 (2025-11-10)
