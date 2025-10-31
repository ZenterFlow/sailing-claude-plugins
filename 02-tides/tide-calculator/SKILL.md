---
name: tide-calculator
description: RYA Yachtmaster tidal height & stream calculator using Admiralty method, secondary-port corrections, and rule-of-twelfths.
license: CC-BY-SA
---

# SKILL: tide-calculator
**RYA Yachtmaster – Tidal Height & Stream Calculator**

## Purpose
Calculate tidal heights and streams for any RYA-standard port, secondary port, or tidal-diamond location, using the official Admiralty method (tidal curves, rule-of-twelfths, time/height differences, computation-of-rates table).

## Activation Triggers
- "calculate tide"
- "tide height at ..."
- "secondary port tide"
- "tidal stream rate"
- "when will tide reach ..."
- "rule of twelfths"

## Behaviour
1. Ask user for:
   - Port / secondary-port name
   - Date & time (UTC or local)
   - Required: height or time
   - Optional: draught & under-keel clearance

2. Work step-by-step (show every number):
   - HW/LW times & heights
   - Range & 1/12th value (if rule-of-twelfths)
   - Secondary-port differences (if applicable)
   - Interpolation for half-hours
   - Final answer with units & datum

3. Warnings:
   - State chart datum
   - Flag irregular tides (Solent, Poole, Victoria BC, etc.)
   - Prefer tidal curve over rule-of-twelfths when curve available

4. Templates & tables:
   - Use `templates/secondary-port.md` for almanac look-ups
   - Use `resources/rule-of-twelfths.md` for quick reference

5. Imperial/metric: accept either, but always state units in answer.

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor-level briefing (loaded into system prompt)
- `resources/` – PNG tables & markdown cheat-sheets
- `templates/` – reusable markdown snippets for worked examples
- `tests/sample-prompts.md` – 5 validation prompts

## Example Session
User: "What is the tide height at 15:30 on 3 July in Victoria? HW 18:00 4.8 m, LW 12:00 1.2 m."  
Skill: returns 3.45 m CD + workings + Victoria BC caveat