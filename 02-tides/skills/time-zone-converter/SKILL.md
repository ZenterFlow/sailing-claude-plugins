---
name: time-zone-converter
description: Maritime time zone conversion between UT/UTC, zone time, and DST using maritime designations (A-Z zones).
license: CC-BY-SA
---

# SKILL: time-zone-converter
**RYA Yachtmaster – Maritime Time Zone Conversion**

## Purpose
Convert between Universal Time (UT), zone times, and Daylight Saving Time using maritime time zone designation systems. Essential for tidal calculations, navigation planning, and interpreting almanac data across international waters.

## Activation Triggers
- "convert to UT"
- "zone time to UTC"
- "what time is HW in BST"
- "time zone conversion"
- "Zone -1 DST to UT"
- "maritime time zones"

## Behaviour
1. Ask user for:
   - Time value (HHMM format)
   - Source time zone (UT/Zone -1/Zone +2/BST/GMT/etc.)
   - Target time zone (if conversion needed)
   - Date (if DST status unclear)

2. Apply conversion rules step-by-step:
   - Identify maritime zone designation (-1, +1, etc.)
   - Check DST status (active or not)
   - Apply zone offset to/from UT
   - Apply DST offset if applicable
   - Show intermediate steps clearly

3. Conversion sequence:
   - **To UT**: Remove DST first → then apply zone conversion
   - **From UT**: Apply zone conversion first → then add DST
   - Always show: `Original → Step 1 → Step 2 → Final`

4. Warnings:
   - Flag if DST status is uncertain
   - Note when date line is crossed (Zone +12/-12)
   - Remind about almanac shaded areas for DST periods
   - State that DST is regional, not universal

5. Common zones:
   - Z (Zulu) = UT = GMT
   - A = Zone -1 (1 hour west of Greenwich)
   - B = Zone -2 (2 hours west)
   - N = Zone +1 (1 hour east)
   - BST = Zone 0 + DST (GMT + 1 hour)

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full conversion rules and safety notes
- `resources/` – zone designation tables, DST rules
- `templates/` – worked conversion examples
- `tests/sample-prompts.md` – 7 validation prompts

## Example Session
User: "Convert 1430 Zone -1 DST to UT"
Skill:
```
Step 1: Remove DST
1430 Zone -1 DST → 1330 Zone -1
(subtract 1 hour for DST)

Step 2: Convert Zone -1 to UT
Zone -1 means subtract 1 hour from UT
So to go TO UT, we add 1 hour
1330 Zone -1 → 1430 UT

Answer: 1430 Zone -1 DST = 1430 UT
```

Note: Zone -1 DST effectively equals UT (the two offsets cancel out).
