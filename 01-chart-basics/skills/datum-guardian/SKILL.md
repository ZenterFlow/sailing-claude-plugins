---
name: datum-guardian
description: Warns if GPS datum and chart geodetic datum differ and gives the position shift to apply.
license: CC-BY-SA
---

# SKILL: datum-guardian
**RYA Yachtmaster – GPS ↔ Chart Datum Guard**

## Purpose
Stop the most common 0.5-mile position error by checking that the GPS datum matches the chart’s geodetic datum; if not, supply the correction to apply before plotting a position.

## Activation Triggers
- "Can I plot WGS-84 on this chart?"
- "Datum shift for BA 1876"
- "GPS says WGS-84, chart says ED-50"
- "Is my position safe to plot?"
- "Datum difference"

## Behaviour
1. Ask for:
   - Chart number (e.g. "BA 2454") or chart title
   - GPS datum currently set (default: WGS-84)

2. Look up the chart’s published geodetic datum:
   - If chart == WGS-84 and GPS == WGS-84 → reply "Safe to plot – no shift required."
   - If datums differ → state the shift in metres & tenths of a minute (lat/long) and the direction to move the fix.

3. Always remind:
   - "Apply the shift to the GPS position BEFORE plotting."
   - "Maximum UK shift ≈ 0.5 nM; elsewhere can exceed 1 nM."

4. Give a one-line worked example when a shift is needed.

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor prompt
- `resources/datum-table.csv` – BA/Imray/NOAA chart ↔ datum list
- `templates/shift-example.md` – canned worked example
- `tests/sample-prompts.md` – 5 validation questions

## Example Session
User: "Can I plot WGS-84 straight onto BA 2454?"  
Skill: "BA 2454 is already WGS-84 – no shift required; plot the position as given."

User: "GPS is WGS-84, chart is ED-50, BA 1876."  
Skill: "Apply 0.3′ N and 0.1′ W to the GPS position before plotting (≈ 370 m shift). Worked example included."