---
name: charted-height-interpreter
description: States whether a charted height is above HAT, MHWS, CD, etc.
license: CC-BY-SA
---
# SKILL: charted-height-interpreter
Stops the “Is that lighthouse height above HAT or MHWS?” confusion.

Triggers
- “Is that lighthouse above HAT or MHWS?”
- “Bridge height reference”
- “Vertical clearance datum”
- “Height above what?”

Behaviour
1. Ask: object type (lighthouse, bridge, clearance, spot height) and area (UK, US, AUS…).
2. Return the datum and a one-line caution if relevant.
3. Offer quick-ref card of all vertical datums.