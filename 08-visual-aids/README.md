# Plugin 08: Visual Aids

**Status**: ✅ Ready for Testing (5 skills implemented)

The Visual Aids Tutor teaches recognition of buoys, lights, cardinal marks, ranges, and transits for safe visual navigation.

## Skills (5 total)

1. **direction-of-buoyage-reminder** - IALA A/B buoyage systems
2. **light-characteristics-quiz** - Interactive quiz for navigation light characteristics (Fl, Oc, Iso, Q, VQ)
3. **cardinal-marks-identifier** - Identify cardinal marks (N/E/S/W) by topmarks, colors, and lights
4. **ranges-and-transits-guide** - Visual ranges and transits for accurate position fixing
5. **dipping-distance-calculator** - Geographic range calculations for lights and objects

## Installation

```bash
/plugin install visual-aids@sailing-curriculum
```

## Usage Examples

### Light Characteristics Quiz
```
User: Test me on navigation light characteristics

Agent: Presents 10-question quiz:
       "What does Fl(3) 15s mean?"
       A) 3 flashes every 15 seconds ✓
       B) Fixed light, 3nm range
       C) Flashing 15 times per second
       D) 3 lights in a row
```

### Cardinal Marks
```
User: I see two black cones pointing up, black over yellow. What is it?

Agent: NORTH CARDINAL MARK
       • Pass NORTH of this mark
       • Topmark: Points up (12 o'clock)
       • Colors: Black over Yellow
       • Light: Q or VQ continuous
       • Hazard is SOUTH of mark
```

### Dipping Distance
```
User: Light is 25m high. My height of eye is 3m. When will I see it?

Agent: DIPPING DISTANCE: 14.0 nautical miles
       Object range: 10.4nm (2.08 × √25)
       Observer range: 3.6nm (2.08 × √3)
       Total: 14.0nm

       Light will rise above horizon at 14nm
```

## Topics Covered

- IALA A/B buoyage systems
- Lateral marks (port/starboard)
- Cardinal marks (N/E/S/W)
- Isolated danger and safe water marks
- Light characteristics (Fl, Oc, Iso, Q, VQ)
- Ranges and transits for position fixing
- Geographic range (dipping distance)
- Visual navigation aids

## Version
v0.2.0 (2025-11-09)
