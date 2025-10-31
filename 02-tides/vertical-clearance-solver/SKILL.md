---
name: vertical-clearance-solver
description: Decide if mast / aerial will hit bridge or wire at predicted HAT or HW springs.
license: CC-BY-SA
---
# SKILL: vertical-clearance-solver
Prevent expensive “crunch” moments.

Triggers
- “Clear 22 m bridge at MHWS + 1.2 m”
- “Mast 19 m, bridge 18 m above HAT, tide +1.0 m – hit?”
- “Overhead cable 15 m, HAT + 0.8 m, will I touch?”

Behaviour
1. Ask: charted height (above HAT), present/future tide, mast (or aerial) height.
2. Available clearance = charted + tide.
3. If available &lt; mast → “MAST HIT by x.x m”, else “SAFE by x.x m”.
4. Remind: “Heights are above HAT; allowance for squat & heel not included.”