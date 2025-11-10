---
name: dipping-distance-calculator
description: Calculate dipping distance (geographic range) for lights and objects based on height and observer height of eye.
license: CC-BY-SA
---

# SKILL: dipping-distance-calculator
**RYA Yachtmaster – Dipping Distance Calculations**

## Purpose
Calculate geographic range (dipping distance) - the maximum distance at which a light or object remains visible above horizon, based on its height and observer's height of eye.

## Activation Triggers
- "dipping distance"
- "geographic range"
- "how far can I see"
- "light range"
- "horizon distance"
- "visible range"

## Behaviour
Calculate using formula: **Range (nm) = 2.08 × √(height in meters)**

For observer + object: **Total Range = 2.08 × (√h₁ + √h₂)**

Where:
- h₁ = object height (meters above sea level)
- h₂ = observer height of eye (meters above sea level)

## Example Output
```
DIPPING DISTANCE CALCULATION
═══════════════════════════════════════

LIGHT: 25m above MHWS
OBSERVER HEIGHT OF EYE: 3m (deck level)

CALCULATION:
─────────────────────────────────────
Object range: 2.08 × √25 = 2.08 × 5 = 10.4nm
Observer range: 2.08 × √3 = 2.08 × 1.73 = 3.6nm

TOTAL GEOGRAPHIC RANGE:
10.4 + 3.6 = 14.0 nautical miles

INTERPRETATION:
✓ Light will rise above horizon at 14nm
✓ This is GEOGRAPHIC range (ignores luminous range)
✓ Actual visibility may be less (weather, light power)

NOTE: Chart shows light range (luminous range in clear weather)
      Dipping distance may be LESS than chart range
      → Whichever is less = when you'll see it
```

## Version
v1.0.0 (2025-11-09)
