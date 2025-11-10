---
name: leeway-applicator
description: Apply leeway correction to True CTS based on wind direction relative to heading.
license: CC-BY-SA
---

# SKILL: leeway-applicator
**RYA Yachtmaster – Leeway Application for CTS**

## Purpose
Apply leeway correction (typically 5-10°) to True CTS based on apparent wind direction.

## Activation Triggers
- "apply leeway"
- "leeway correction"
- "wind effect CTS"

## Behaviour
Rules:
- **Port tack** (wind from port): SUBTRACT leeway from True CTS
- **Starboard tack** (wind from starboard): ADD leeway to True CTS
- Typical leeway: 5° light, 10° moderate, 15° heavy

Example: True CTS 045°T, leeway 8° port tack → 045° - 8° = 037°T (magnetic course before variation)

## Version
v1.0.0 (2025-11-10)
