---
name: tidal-terminology
description: Master tidal terminology (MHWS, MLWS, MHWN, MLWN, HAT, LAT, Chart Datum) and vertical datums for safe depth calculations and exam prep.
license: CC-BY-SA
---

# SKILL: tidal-terminology
**RYA Yachtmaster – Tidal Terminology and Vertical Datums**

## Purpose
Define and explain tidal terminology (MHWS, MLWS, MHWN, MLWN, HAT, LAT, Chart Datum), understand vertical reference planes, and apply these concepts to depth calculations, bridge clearances, and chart interpretation for safe navigation and exam preparation.

## Activation Triggers
- "what is MHWS"
- "chart datum"
- "HAT vs LAT"
- "drying height"
- "tidal terminology"
- "vertical datums"
- "bridge clearance datum"
- "MLWS MLWN MHWS MHWN"
- "what's the difference between charted depth and drying height"

## Behaviour
1. **Educational Mode**: Provide clear definitions with visual diagrams
   - Use ASCII diagrams from templates
   - Show vertical datum relationships
   - Explain Chart Datum as the reference plane
   - Demonstrate practical applications

2. **Interactive Teaching**:
   - Quiz on terminology definitions
   - Test understanding with worked examples
   - Correct common misconceptions (CD vs sea level, HAT vs MHWS)
   - Show when to use each datum

3. **Key Terminology Covered**:
   - **Chart Datum (CD)**: Zero reference for charted depths (≈ LAT)
   - **HAT**: Highest Astronomical Tide (used for bridge clearances)
   - **LAT**: Lowest Astronomical Tide (≈ Chart Datum)
   - **MHWS**: Mean High Water Springs
   - **MLWS**: Mean Low Water Springs
   - **MHWN**: Mean High Water Neaps
   - **MLWN**: Mean Low Water Neaps
   - **Range**: HW height - LW height
   - **Drying heights**: Heights above CD that uncover at low tide

4. **Practical Applications**:
   - Bridge clearances (usually HAT, sometimes MHWS)
   - Light elevations (usually MHWS)
   - Depth calculations (CD + tide height)
   - Drying heights (tide must exceed drying height)

5. **Use Templates**:
   - `templates/vertical-datum-diagram.md` for visual hierarchy
   - `templates/depth-calculations.md` for worked examples
   - `templates/datum-definitions.md` for quick reference

6. **Exam Focus**:
   - 100% accuracy on term definitions
   - Identify correct datum for clearances from chart notes
   - Calculate total depth and under-keel clearance
   - Distinguish drying heights from charted depths

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor-level briefing
- `templates/` – educational diagrams and examples
- `resources/` – reference materials and cheat sheets
- `tests/sample-prompts.md` – 7 test questions

## Example Session
**User**: "What's the difference between Chart Datum and MHWS?"
**Skill**: "Chart Datum (CD) is the reference plane for all charted depths - it's set at approximately LAT (Lowest Astronomical Tide), the lowest the tide can go.

MHWS (Mean High Water Springs) is the average height of high water during spring tides, typically 4-7 meters ABOVE Chart Datum depending on location.

**Practical difference**:
- Charted depths are measured DOWN from CD (always water)
- Light elevations are measured UP from MHWS
- Bridge clearances are usually UP from HAT (even higher than MHWS)

[Shows diagram from templates/vertical-datum-diagram.md]

Would you like me to show you how to calculate total depth using CD, or explain HAT for bridge clearances?"
