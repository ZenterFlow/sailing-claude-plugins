---
name: light-characteristics-quiz
description: Interactive quiz for identifying navigation light characteristics (Fl, Oc, Iso, Q, VQ) and rhythms for vessel and buoy identification.
license: CC-BY-SA
---

# SKILL: light-characteristics-quiz
**RYA Yachtmaster – Light Characteristics Identification Quiz**

## Purpose
Train recognition of navigation light characteristics through interactive quizzes. Master identifying light rhythms (Fl, Oc, Iso, Q, VQ, LFl, etc.) essential for vessel identification, buoy recognition, and lighthouse identification at night.

## Activation Triggers
- "light characteristics quiz"
- "identify lights"
- "test me on lights"
- "navigation lights quiz"
- "light rhythm"
- "flashing lights"

## Behaviour
1. **Quiz Mode**: Present light characteristic and ask for identification
2. **Explanation Mode**: Explain light characteristic when asked
3. **Practice Mode**: Random quizzes with immediate feedback

**Light Characteristics Covered**:
- **F** - Fixed (continuous light)
- **Fl** - Flashing (<2 sec light, >2 sec dark)
- **LFl** - Long Flashing (≥2 sec flash)
- **Oc** - Occulting (light > dark)
- **Iso** - Isophase (light = dark)
- **Q** - Quick (50-60 flashes/min)
- **VQ** - Very Quick (100-120 flashes/min)
- **UQ** - Ultra Quick (240-300 flashes/min)
- **Al** - Alternating (changes color)

**Quiz Format**:
```
NAVIGATION LIGHT QUIZ - Question 1/10
═══════════════════════════════════════

Light characteristic: Fl(3) 10s 15m 12M

What does this mean?

A) Flashing white, 3 flashes every 10 seconds
B) Fixed light, 3 nautical miles range
C) Occulting light, flashes 3 times
D) Quick flashing, 10 second intervals

[User answers]

✓ CORRECT! Fl(3) 10s means:
- Flashing light
- 3 flashes in a group
- Complete cycle every 10 seconds
- Height: 15m above MHWS
- Range: 12 nautical miles
```

## Example Session
User: "Test me on light characteristics"

Returns 10-question quiz covering:
- Flashing patterns (Fl, Oc, Iso)
- Quick and very quick flashes (Q, VQ)
- Group flashing Fl(2), Fl(3), etc.
- Composite characteristics Fl(2+1)
- Color identification (W, R, G, Y)
- Height and range interpretation

## Teaching Notes
- Period = time for complete cycle (not just flash time)
- Occulting = mostly light with brief dark periods
- Flashing = mostly dark with brief light periods
- Quick/VQ are VERY fast (count impossible by eye)
- Height is above MHWS, range is nominal range
- Color: W=white (default), R=red, G=green, Y=yellow

## Version
v1.0.0 (2025-11-09)
