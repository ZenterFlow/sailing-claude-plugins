---
name: compass-dip-heeling
description: Understand magnetic dip and heeling error effects on compass accuracy, with mitigation strategies.
license: CC-BY-SA
---

# SKILL: compass-dip-heeling
**RYA Yachtmaster – Compass Dip and Heeling Error Awareness**

## Purpose
Teach understanding of magnetic dip principles, hemisphere-specific compass balancing requirements, heeling error effects, and practical mitigation strategies for accurate compass navigation.

## Activation Triggers
- "Magnetic dip"
- "Compass dip"
- "Heeling error"
- "Compass balance hemisphere"
- "Northern hemisphere compass"
- "Southern hemisphere compass"
- "Sluggish compass"
- "Compass not level"

## Behaviour
1. Identify the user's learning need:
   - **Dip principles**: Understanding magnetic dip physics
   - **Hemisphere balancing**: Why compasses are region-specific
   - **Heeling error**: Effects of vessel heel on compass accuracy
   - **Troubleshooting**: Diagnosing dip/heeling problems
   - **Mitigation**: Practical strategies to minimize errors

2. For magnetic dip explanation:
   - Explain Earth's magnetic field geometry
   - Show how field lines curve into Earth
   - Explain dip angle concept (inclination)
   - Describe hemisphere-specific effects
   - Introduce isoclinic lines and aclinic line (magnetic equator)

3. For compass balancing:
   - Explain why needles need weighting
   - Describe hemisphere-specific balance requirements
   - Discuss consequences of improper balance
   - Mention global/universal compasses
   - Show how to identify balance problems

4. For heeling error:
   - Explain the mechanism (vertical forces becoming horizontal)
   - Show relationship to heel angle
   - Describe effects on different headings
   - Explain why sailing vessels more affected
   - Teach practical recognition

5. For mitigation strategies:
   - Keep vessel reasonably upright during critical nav work
   - Use level compass mounting when possible
   - Take bearings at consistent heel angles
   - Understand when errors are significant vs. negligible
   - Know when to suspect heeling error problems

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor prompt with physics
- `templates/dip-diagram.md` – visual explanation of magnetic dip
- `templates/heeling-error-guide.md` – practical error recognition
- `templates/hemisphere-balance-chart.md` – compass balance reference
- `tests/sample-prompts.md` – validation questions
- `resources/dip-angles-reference.md` – global dip angle data
- `resources/troubleshooting-guide.md` – diagnosing dip/heeling issues

## Example Session

**User:** "What is magnetic dip and why does it matter?"

**Skill:**
```
MAGNETIC DIP EXPLAINED

WHAT IS IT?
Magnetic dip (inclination) is the angle at which Earth's
magnetic field lines intersect the surface.

THE PHYSICS:
- Earth's magnetic field resembles a bar magnet
- Field lines curve from south pole to north pole
- At equator: field lines run horizontally (0° dip)
- At poles: field lines run vertically (90° dip)
- Everywhere else: field lines angle into Earth

HEMISPHERE EFFECTS:

Northern Hemisphere (positive dip):
  - Magnetic field lines point DOWNWARD into Earth
  - Compass needle north end pulled down
  - Dip angle: 0° (equator) to +90° (north magnetic pole)
  - Example: London ~67°, New York ~70°

Southern Hemisphere (negative dip):
  - Magnetic field lines point DOWNWARD into Earth
  - Compass needle south end pulled down
  - Dip angle: 0° (equator) to -90° (south magnetic pole)
  - Example: Sydney ~65°, Cape Town ~60°

WHY IT MATTERS:
1. Compass needles must be BALANCED for local dip
2. Unbalanced compass = sluggish, inaccurate readings
3. Northern compass in southern waters WILL malfunction
4. Creates friction on pivot, reducing sensitivity

🧭 ISOCLINIC LINES:
Lines of equal dip angle on globe
- Magnetic equator (aclinic line): 0° dip
- Roughly follows geographic equator
- Varies by longitude (Earth's field not perfectly uniform)
```

**User:** "My compass seems sluggish. Could this be dip error?"

**Skill:**
```
COMPASS SLUGGISH? DIP ERROR DIAGNOSIS

SYMPTOMS OF DIP IMBALANCE:
✗ Compass card slow to settle after turn
✗ Erratic or sticky movement
✗ Card appears to drag or bind
✗ Reduced sensitivity to heading changes
✗ Card sits at angle (not level)

QUESTIONS TO ASK:

1. Has vessel changed hemisphere?
   → Northern compass in southern waters?
   → Southern compass in northern waters?
   → Recently sailed across equator?

2. What is local dip angle?
   → High latitude (>60°)? Strong dip forces
   → Near equator (<20°)? Minimal dip forces

3. Is compass marked for hemisphere/zone?
   → "Northern Hemisphere" or "NH"
   → "Southern Hemisphere" or "SH"
   → "Global" or "Universal" (rare, expensive)
   → Zone numbers (1-5, specific latitude bands)

FIXES:

Immediate (no hardware change):
  - Accept reduced accuracy
  - Take bearings carefully, let card settle fully
  - Cross-check with GPS when possible
  - Avoid relying on small course corrections

Permanent:
  - Replace with properly balanced compass
  - Consider global compass if crossing zones
  - Check zone markings before buying replacement

⚠️ PREVENTION:
When planning long passages:
- Check compass hemisphere compatibility
- Carry properly balanced spare if crossing equator
- Budget for compass replacement if relocating
```

**User:** "What is heeling error?"

**Skill:**
```
HEELING ERROR EXPLAINED

THE PROBLEM:
When a vessel heels, magnetic forces change direction
relative to the compass, creating deviation errors.

THE MECHANISM:

Vessel Upright:
  [Compass level]
  - Vertical magnetic forces act straight down
  - Horizontal forces act in plane of compass card
  - Compass reads correctly

Vessel Heeled:
  [Compass tilted]
  - Vertical forces now have HORIZONTAL component
  - Horizontal forces now have VERTICAL component
  - Creates false deviation reading
  - Error proportional to heel angle

CHARACTERISTICS:
- Increases with heel angle
- Varies with heading (worst on some courses)
- Cannot be corrected with standard deviation table
- Significant in sailing vessels when hard on wind
- Minimal in powerboats (limited heel)

WHEN IT'S SIGNIFICANT:
✗ Sailing vessel heeled >15-20°
✗ Heavy weather, working to windward
✗ Critical navigation in confined waters
✗ Taking bearings while heeled

WHEN IT'S NEGLIGIBLE:
✓ Powerboat normal operation (<5° heel)
✓ Sailing vessel upright or light heel
✓ Downwind sailing (minimal heel)

MITIGATION STRATEGIES:

1. Keep vessel reasonably upright during critical work
   - Ease sheets briefly for important bearing
   - Time navigation for less demanding points of sail
   - Slow down in powerboat to reduce rolling

2. Consistent technique
   - Take related bearings at same heel angle
   - Note heel condition in log with bearing

3. Awareness
   - Know when heeling error likely
   - Cross-check with GPS/radar when heeled
   - Add uncertainty margin to heeled bearings

4. Compass mounting
   - Gimballed compass reduces error (stays level)
   - Flat-mounted compass shows full heeling error

⚠️ SAFETY NOTE:
Heeling error is systematic but unpredictable.
When sailing heeled in confined waters, add safety
margin to all compass-based navigation decisions.

💡 PRACTICAL TEST:
Sail same heading on both tacks. Different compass
readings = heeling error present.
```

## Key Concepts
- **Magnetic dip**: Angle of Earth's field relative to surface (inclination)
- **Hemisphere balance**: Compass needles weighted for specific latitude zones
- **Isoclinic lines**: Lines of equal dip angle (0° at magnetic equator)
- **Heeling error**: Compass deviation caused by vessel heel angle
- **Sluggish compass**: Primary symptom of dip imbalance
- **Vertical/horizontal force conversion**: Mechanism of heeling error
- **Global compass**: Expensive compass balanced for all latitudes
- **Gimballed mounting**: Reduces heeling error by keeping compass level
