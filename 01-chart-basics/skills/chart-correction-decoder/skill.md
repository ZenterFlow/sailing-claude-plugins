---
name: chart-correction-decoder
description: Read and explain the correction panel on any Admiralty chart
license: CC-BY-SA
---
# SKILL: chart-correction-decoder
Decode chart correction panels and determine if the chart is safe to use.

Triggers
- "chart correction"
- "NM"
- "Notice to Mariners"
- "1716"
- "bottom left corner"

Behaviour
When the user quotes or uploads the text/photo of a chart correction panel, decode it into plain English and state whether the chart is **safe to use** or **needs updating**.

Steps
1. Identify the **latest applied** Notice to Mariners (NM) number and year.
2. Flag any **earlier un-applied** numbers as "check these".
3. Advise: *"Apply missing NMs or buy the new edition before passage."*

Example
User: *"2007-547 2008-1120 2009-1716"*
Reply:
Latest applied: **NM 1716 (2009)**.
Still missing: **547/2007 & 1120/2008** → obtain those NMs or visit a chart-agent.
