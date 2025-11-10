---
name: magnetic-variation-calculator
description: Calculate current magnetic variation from chart compass rose data using base year and annual change rate.
license: CC-BY-SA
---

# SKILL: magnetic-variation-calculator
**RYA Yachtmaster – Magnetic Variation Calculator**

## Purpose
Calculate the current magnetic variation for a given location and year using compass rose data from charts, accounting for annual change rates to get accurate True ↔ Magnetic conversions.

## Activation Triggers
- "Calculate variation for 2025"
- "Variation was 7°W in 2005, annual change 8' E"
- "Update variation from compass rose"
- "What's the current variation?"
- "Variation calculation"
- "Apply annual change to variation"

## Behaviour
1. Ask for (if not provided):
   - Base year variation (e.g., "7° 25' W in 2005")
   - Annual change rate (e.g., "8' E" or "8' East")
   - Target year (e.g., "2025")

2. Calculate the variation:
   - Determine years elapsed: Target Year - Base Year
   - Calculate total change: Annual Rate × Years Elapsed
   - Apply change using directional rules:
     * West variation + East movement: SUBTRACT change
     * West variation + West movement: ADD change
     * East variation + West movement: SUBTRACT change
     * East variation + East movement: ADD change

3. Show full working:
   - Display calculation steps clearly
   - Convert minutes to degrees if needed
   - Round to nearest degree for practical use
   - State final variation with direction (E or W)

4. Provide context:
   - "Use this variation for all T↔M conversions in this area"
   - "Re-check compass rose if chart is 5+ years old"
   - "Variation changes slowly – annual update usually sufficient"

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor prompt
- `templates/worked-example.md` – step-by-step calculation example
- `templates/directional-rules.md` – quick reference for E/W logic
- `tests/sample-prompts.md` – validation questions

## Example Session
**User:** "Variation was 7° 25' W in 2005, annual change 8' E. What's it now in 2025?"

**Skill:**
```
MAGNETIC VARIATION CALCULATION

Base Data:
- Year: 2005
- Variation: 7° 25' W
- Annual Change: 8' E (moving eastward)

Target Year: 2025
Years Elapsed: 2025 - 2005 = 20 years

Total Change:
8' × 20 = 160' = 2° 40'

Application Rule:
West variation + East movement → SUBTRACT the change

Calculation:
7° 25' W - 2° 40' = 4° 45' W

✅ CURRENT VARIATION (2025): 5° W
(Rounded to nearest degree for practical navigation)

Use 5° W for all True ↔ Magnetic conversions in this area.
```

## Key Concepts
- **Variation moves slowly**: Typical rates 5-15' per year
- **Direction matters**: East/West application reverses based on movement direction
- **Practical rounding**: Round to nearest degree for standard navigation
- **Geographic variation**: Changes by location – always use local compass rose
- **Agonic line**: 0° variation line where True North = Magnetic North
