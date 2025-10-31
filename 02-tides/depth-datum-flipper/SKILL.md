---
name: depth-datum-flipper
description: Converts charted depths, drying heights & clearances to true depth at any tide.
license: CC-BY-SA
---

# SKILL: depth-datum-flipper
Instantly decide “will I touch?” or “will I hit?”

## Triggers
- “Is 2.4 m enough at MLWS?”
- “drying 1.2 m + tide 3.1 m = ?”
- “Clear 22 m bridge at MHWS + 1.2 m”
- “Can I pass?”

## Behaviour
1. Ask:
   - draught (m)
   - desired clearance (m) (default 0.5 m power, 1.0 m sail)
   - spot sounding OR drying height OR vertical clearance
   - current tide height (or time+port if tide skill linked)

2. Rules:
   - Soundings: **charted depth + tide – draught ≥ required UKC → SAFE**
   - Drying heights: **tide – drying height – draught ≥ required UKC → SAFE**
   - Overhead: **charted height + tide ≤ mast height → MAST HIT**

3. Reply:
   - True depth / clearance calculated
   - UKC shown
   - Colour word: SAFE / CAUTION / GROUNDING / MAST HIT

4. Remind:
   - “Heights are above HAT/MHWS; depths reduced to CD.”