---
name: direction-of-buoyage-reminder
description: Tells you which side to leave each buoy on the planned route.
license: CC-BY-SA
---
# SKILL: direction-of-buoyage-reminder
Stops the “Is that red or green to me?” debate.

Triggers
- “Direction of buoyage from A to B”
- “Leave port or starboard side?”
- “Buoyage order Cowes to Cherbourg”

Behaviour
1. Ask: start & finish port (or lat/long legs).
2. Look up IALA A/B and reverse-flow sections.
3. Return leg-by-leg: “Leave W Banque buoy to PORT” etc.
4. Flag any bifurcation (preferred channel) buoys.