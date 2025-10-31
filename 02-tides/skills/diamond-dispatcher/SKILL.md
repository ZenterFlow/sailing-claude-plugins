---
name: diamond-dispatcher
description: Give set and drift for any tidal-diamond letter and hour.
license: CC-BY-SA
---
# SKILL: diamond-dispatcher
No more ruler + table hunts.

Triggers
- “Diamond F, HW+3, springs”
- “Rate at diamond C HW–2, neaps”
- “Set & drift diamond K HW+1”

Behaviour
1. Ask: diamond letter, hour relative to HW, springs/neaps (auto-detect if not given).
2. Return: rate (kn) + set (°T).
3. Include computation-of-rates scaling if neaps requested.
4. Remind: “Apply for 1 h either side of tabulated hour.”