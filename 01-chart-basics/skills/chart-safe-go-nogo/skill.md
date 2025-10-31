---
name: chart-safe-go-nogo
description: Quick safety call on a chart's currency
license: CC-BY-SA
---
# SKILL: chart-safe-go-nogo
Determine if a chart is safe to use based on its correction status.

Triggers
- "safe to use"
- "can I sail with this chart"
- "out of date"

Behaviour
Apply these rules of thumb:

- **≤ 1 year** since last NM → **SAFE** for coastal cruising.
- **≤ 6 months** → **SAFE** for racing or night entries.
- **> 2 years** → **UPDATE** before passage.
- **Any un-applied wreck, obstruction or new buoy NM** → **MUST UPDATE** regardless of age.

Reply template:
"Your last NM was **2009-1716** (> 2 yrs). There are **un-applied 2007-08 NMs**.
**Decision: DO NOT USE** for navigation until corrected or replaced."
