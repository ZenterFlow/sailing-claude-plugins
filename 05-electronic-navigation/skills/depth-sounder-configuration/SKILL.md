---
name: depth-sounder-configuration
description: Calibrate depth sounder offset settings and use depth for navigation verification.
license: CC-BY-SA
---

# SKILL: depth-sounder-configuration
**RYA Yachtmaster – Depth Sounder Configuration and Usage**

## Purpose
Calibrate and configure depth sounder offset settings, understand accuracy limitations, and use depth for navigation verification.

## Activation Triggers
- "depth sounder offset"
- "echo sounder calibration"
- "depth alarm settings"
- "sounder accuracy"

## Behaviour
**Three Offset Calibration Methods**:

1. **From Keel/Max Draft**:
   - When reading = 0, vessel touches bottom
   - Advantage: Immediate safety warning
   - Disadvantage: Must add draught for actual depth
   - Best for: Shallow water navigation, grounding avoidance

2. **From Waterline**:
   - Reading matches charted depth (with tide applied)
   - Advantage: Easy chart comparison
   - Disadvantage: Calculation needed for keel clearance
   - Best for: Navigation using contours

3. **From Transducer (No Offset)**:
   - Raw transducer data
   - Advantage: No artificial error
   - Disadvantage: Mental math required
   - Best for: Technical accuracy, troubleshooting

**Accuracy Limitations**:
- Over soft mud: Reads deeper (signal penetrates)
- Going astern: Propeller wash disrupts signal
- Large fish/shoals: False readings
- Crossing wakes: Bubbles block signal
- Deep water >100m: Signal dissipates
- Temperature layers: Refraction errors

**Navigation Verification**:
Formula: Expected depth = Charted depth + Tidal height
- Compare sounder reading to expected
- If depth < expected → off track or hazard
- Set minimum depth alarm for each leg

**Accuracy Check**:
- Use lead line at known depth (sill, tidal gauge)
- Compare to sounder reading
- Adjust offset if needed
- Check regularly, especially on new vessel

## Version
v1.0.0 (2025-11-10)
