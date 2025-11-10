---
name: tidal-hour-selector
description: Determine correct tidal hour offset for CTS based on trip duration and departure time.
license: CC-BY-SA
---

# SKILL: tidal-hour-selector
**RYA Yachtmaster – Tidal Hour Selection for CTS**

## Purpose
Determine which tidal hour (HW-6 to HW+6) to use for CTS calculation based on trip midpoint.

## Activation Triggers
- "which tidal hour"
- "select tide for CTS"
- "tidal hour CTS"

## Behaviour
Process:
1. Calculate trip duration (distance ÷ speed)
2. Find midpoint time (departure + duration/2)
3. Convert to HW reference time
4. Select nearest HW±N hour from diamond/atlas
5. Extract set/drift for that hour

Trips >2 hours: Consider multi-hour integration

## Version
v1.0.0 (2025-11-10)
