---
name: visual-fix-calculator
description: Calculate vessel position using visual bearings, ranges, and transits with cocked hat error assessment.
license: CC-BY-SA
---

# SKILL: visual-fix-calculator
**RYA Yachtmaster – Visual Position Fixing**

## Purpose
Calculate vessel position using compass bearings, ranges, and transits. Assess fix quality using cocked hat size and bearing geometry. Validates three-point fixes and identifies systematic errors.

## Activation Triggers
- "three point fix"
- "visual position fix"
- "compass bearing fix"
- "cocked hat"
- "running fix"
- "position from bearings"
- "two bearing fix"
- "cross bearing"

## Behaviour
1. Ask user for:
   - 2-3 compass bearings to charted objects
   - Vessel deviation (if known)
   - Magnetic variation (from chart)
   - Optional: range or transit for additional validation

2. Work step-by-step (show every calculation):
   - Convert compass bearings to true bearings
   - Check bearing geometry (ideal 60° apart, acceptable 30-150°)
   - Plot position lines (reciprocal bearings)
   - Assess cocked hat size (warn if >0.5 nm)
   - Identify most reliable position (center of cocked hat or weighted)

3. Quality Assessment:
   - **EXCELLENT**: 3 bearings 60° apart, cocked hat <0.1 nm
   - **GOOD**: 3 bearings 40-80° apart, cocked hat <0.3 nm
   - **ACCEPTABLE**: 2-3 bearings 30-150° apart, cocked hat <0.5 nm
   - **POOR**: Bearings <30° or >150° apart, cocked hat >0.5 nm
   - **SUSPECT**: Systematic error indicated (one bearing way off)

4. Warnings:
   - Flag poor bearing geometry
   - Warn if cocked hat too large (re-take bearings)
   - Suggest removing suspect bearing if one is clearly wrong
   - Remind to use most prominent/accurate objects

5. Running Fix Support:
   - Advance first position line by course and distance
   - Calculate transferred position
   - Warn about accumulated errors

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor-level briefing
- `resources/bearing-geometry.md` – bearing angle guidelines
- `templates/three-point-fix.md` – worked example template
- `templates/running-fix.md` – running fix example
- `tests/sample-prompts.md` – 5 validation prompts

## Example Session
User: "I have bearings: North Head 045°C, South Light 110°C, East Point 160°C. Deviation 2°W, Variation 5°E."

Skill returns:
```
VISUAL POSITION FIX
─────────────────────────────────────
Bearings (Compass → True):
• North Head:  045°C + 2° (dev) + 5° (var) = 052°T → Plot reciprocal 232°T
• South Light: 110°C + 2° + 5° = 117°T → Plot reciprocal 297°T
• East Point:  160°C + 2° + 5° = 167°T → Plot reciprocal 347°T

Bearing Geometry:
• North Head to South Light: 65° ✓ GOOD
• South Light to East Point: 50° ✓ GOOD
• East Point to North Head: 245° (115° complementary) ✗ POOR

Assessment: ACCEPTABLE (2 good angles, 1 poor)

Cocked Hat: ~0.2 nm

Position: Center of cocked hat
Estimated: 50°42.5'N, 001°15.3'W

QUALITY: GOOD FIX
✓ Use for navigation
⚠ Consider re-taking bearings for better geometry
```

## Teaching Notes
- "Quick is better than perfect" - take bearings rapidly
- Take most reliable bearing last (it changes slowest)
- Always plot reciprocal of bearing from ship
- Cocked hat should be small enough to navigate safely
- If large cocked hat: check for systematic error or take new bearings
- Running fix: useful when only one object available, but less accurate

## Version
v1.0.0 (2025-11-09)
