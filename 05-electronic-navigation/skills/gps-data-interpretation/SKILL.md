---
name: gps-data-interpretation
description: Interpret GPS data fields (SOG, COG, XTE, TTG, VMG) for navigation decisions.
license: CC-BY-SA
---

# SKILL: gps-data-interpretation
**RYA Yachtmaster – GPS Data Field Interpretation**

## Purpose
Interpret key GPS data fields (SOG, COG, XTE, TTG, VMG), understand their relationships, and apply for navigation decisions.

## Activation Triggers
- "what is SOG"
- "what is XTE"
- "GPS data fields"
- "velocity made good"
- "cross track error"

## Behaviour
**Key GPS Data Fields**:

**SOG (Speed Over Ground)**:
- GPS-calculated speed using fix-to-fix positions
- **Includes tide and leeway effects**
- Formula: Distance between fixes ÷ time
- Compare to log speed (water speed only) to determine tidal drift

Example: Log 5 kn + 4 kn favorable tide = SOG 9 kn

**COG (Course Over Ground)**:
- Direction of movement over ground (not heading)
- Differs from compass heading due to tide/leeway
- Derived from successive position fixes

**XTE (Cross Track Error)**:
- Lateral distance from planned ground track
- Display: "0.3M Port" or arrow showing direction
- **Uses**:
  - Monitor track deviation
  - Trigger tacking decisions (e.g., tack when XTE >0.5 nm)
  - Set alarms for TSS or narrow channels

**TTG (Time To Go)**:
- Time to waypoint at current SOG
- Formula: (Distance ÷ SOG) × 60 = minutes
- **Assumes constant SOG** - adjust for tidal changes!

**VMG (Velocity Made Good)**:
- Speed component directly toward destination
- Essential for tacking/zigzag courses
- Shows efficiency: 5 kn boat speed might = 3 kn VMG when tacking

**Critical Comparisons**:
- SOG vs Log Speed = Tidal effect + leeway
- COG vs Heading = Tidal set
- VMG vs SOG = Course efficiency

## Version
v1.0.0 (2025-11-10)
