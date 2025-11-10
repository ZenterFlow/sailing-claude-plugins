# Leading Lines and Transit Navigation

---
name: leading-lines-transit
version: 1.0.0
triggers:
  - "leading lines"
  - "leading lights"
  - "transit navigation"
  - "lower light rule"
  - "charted transit"
  - "compass deviation check"
---

## Purpose

Execute precise navigation using charted and improvised leading lines for both day and night pilotage, including course correction techniques and compass deviation checks.

## Activation Triggers

This skill activates when you ask about:
- Leading lines or charted transits
- Leading lights operation
- Lower light rule for corrections
- Transit navigation techniques
- Compass deviation checks using transits

## Behavior

### Charted Transits

**Chart Symbol**: Magenta line with direction arrow

**Bearing Information**: Always given as TRUE bearing toward the transit objects

**Day Use**: Align prominent objects
- Cones and diamonds (navigation marks)
- Church spires
- Chimneys
- Distinctive buildings
- Natural features (summits, headlands)

**Example**: "Chimney and church spire at Seaview in transit (048°) lead into quay"

**Chart Reading**:
- Find magenta line on chart
- Note true bearing printed alongside
- Identify objects to align
- Convert to magnetic for hand compass use

### Leading Lights Operation

**Configuration**: Two lights at different heights
- Rear light: HIGHER elevation
- Front light: LOWER elevation

**Light Sequences**: Distinct patterns to identify each light

**Typical Characteristics**:
- **Rear Light**: Iso 4s (2 seconds lit, 2 seconds dark)
- **Front Light**: Iso 2s (1 second lit, 1 second dark)
- Different patterns allow identification

**Alignment**: When lights are vertically aligned, vessel is on transit line

**Operation**:
- Maintain charted true bearing (convert to magnetic)
- Keep lights vertically stacked
- Adjust course to maintain alignment

**Example**: Transit bearing 148°T, variation 6°W → Steer 142°M keeping lights aligned

### The Lower Light Rule

**Course Correction Principle**: ALWAYS steer toward the lower light

**Off-Track Scenarios**:
- **Lower light LEFT of higher light**: Turn LEFT (port) to align
- **Lower light RIGHT of higher light**: Turn RIGHT (starboard) to align

**Universal Application**:
- Works for entering port
- Works for leaving port
- Direction of travel doesn't matter

**Why It Works**:
- Lower light position directly indicates required turn direction
- Geometric relationship holds regardless of your direction
- Simple, intuitive, never fails

### Entering vs Leaving Port

**Entering**:
- Line bow with higher (rear) light
- Look forward at lights
- Steer to keep lights aligned
- Apply lower light rule if misaligned

**Leaving**:
- Line stern with higher (rear) light
- Look over shoulder (astern)
- Steer to keep lights aligned
- Apply lower light rule if misaligned

**Key Point**: Lower light rule DOES NOT reverse when leaving

**Mnemonic**: Lower light position shows turn direction regardless of travel direction

### Improvised Transits

**Creation**: Use any two prominent charted objects in suitable alignment

**Advantages**:
- Custom navigation aid for specific destinations
- No official transit needed
- Flexible approach planning

**Selection Criteria**:
- Both objects charted and identifiable
- Good separation (vertical or horizontal)
- Clear line of sight
- Alignment leads through safe water

**Verification**:
- Test alignment against chart
- Ensure objects remain distinct
- Check safe water along entire line

**Chart Limitation**: Not marked as magenta line, but usable if objects reliable

**Example**: "When chimney and radio mast align, turn to port - leads between rocks"

### Compass Deviation Check Using Transits

**Method**:
1. Identify established transit with known true bearing
2. Sail across transit on various headings
3. At moment of crossing, take compass bearing of transit line
4. Compare compass reading to known true bearing (corrected for variation)
5. Calculate deviation for that heading

**Deviation Formula**:
```
Deviation = Compass Bearing - (True Bearing ± Variation)
```

**Multiple Headings**:
- Repeat on different compass headings (N, NE, E, SE, S, SW, W, NW)
- Create deviation curve for all headings
- Note maximum deviation values

**Advantages of Transit Method**:
- Precise known bearing reference
- Easy to identify crossing moment
- Repeatable measurement
- All boat headings testable

### Integration with Pilotage Planning

**Depth Monitoring**:
- Monitor depth contours along transit line
- Add Height of Tide (HOT) to charted depths
- Expect specific depths at points along transit

**Pilot Plan Format**:
- Leg number
- Transit bearing (magnetic)
- Distance along transit
- Minimum depth + HOT
- Visual confirmation points

**Animation/Visualization**:
- Day: Watch objects align
- Night: Watch lights stack vertically
- Both: Monitor depth gauge

### Operational Best Practices

**Avoid Oscillation**:
- Make small corrections
- Don't over-steer
- Smooth helm movements
- Anticipate vessel response

**Light Identification**:
- Confirm front vs rear by light sequence
- Check chart for characteristics
- Verify both lights visible before committing

**Backup Methods**:
- Use depth as secondary check
- Note GPS position periodically
- Monitor other navigation marks

### Common Errors to Avoid

❌ Turning away from lower light (wrong direction)
❌ Thinking correction reverses when leaving port
❌ Using charted true bearing directly with hand bearing compass
❌ Misidentifying front vs rear lights by sequence
❌ Over-correcting and oscillating around transit line
❌ Not verifying both lights visible before approach
❌ Forgetting to apply variation for compass work

### Assessment Criteria

You should be able to:
- Identify safe approach bearing from charted transit information
- Determine required turn from given light misalignment scenario
- Construct improvised transit using charted objects
- Explain why course correction does NOT reverse between entering and leaving
- Calculate compass deviation from transit bearing data
- Apply lower light rule correctly in all situations

### Practical Application

**Scenario**: Leading lights misaligned - lower light to starboard of upper light

1. **Analysis**: Lower light is RIGHT of higher light
2. **Action**: Turn RIGHT (starboard)
3. **Result**: Lights align, vessel returns to transit line
4. **Applies**: Both entering and leaving port

**Scenario**: Charted transit 048°T, variation 6°W

1. **Conversion**: Magnetic = 048° - 6° = 042°M
2. **Execution**: Steer 042°M keeping objects/lights aligned
3. **Verification**: Monitor depth and position
4. **Correction**: Apply lower light rule if misaligned

**Scenario**: Check compass deviation using transit

1. **Transit bearing**: 325°T, variation 6°W → 319°M expected
2. **Cross transit**: Sail across line on heading 090°C
3. **Compass reading**: Transit bears 322°C
4. **Deviation**: 322°C - 319°M = 3°E deviation on heading 090°
5. **Record**: Note "090° heading: 3°E deviation"

---

**Version**: 1.0.0 (v1.1.0 - 2025-11-10)
