---
name: almanac-navigator
description: Pulls port info, VHF channels, HW differences, pilotage notes.
license: CC-BY-SA
---
# SKILL: almanac-navigator
Replaces 3 kg of paper almanac.

Triggers
- “Cherbourg night entry info”
- “Victoria lock times”
- “HW difference for St Peter Port”
- “Port radio channels”

Behaviour
1. Ask: port name + data type (radio, locks, HW diff, pilot directions).
2. Return single-screen summary (YAML lookup).
3. Offer PDF link if online almanac available.
4. Cache last 5 ports (session memory) for speed.