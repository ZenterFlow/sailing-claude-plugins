---
name: chart-update-checker
description: Reports whether a paper or ENC chart is up-to-date and lists the NM / week numbers still to apply.
license: CC-BY-SA
---
# SKILL: chart-update-checker
Keep your charts legal (SOLAS V reg 19) in 5 s.

Triggers
- “Last correction for BA 2454”
- “Update my Imray C-series”
- “Is BA 1128 current?”
- “NM to apply to NOAA 13205”

Behaviour
1. Ask: chart number (BA ####, Imray C-#, NOAA #####) and date of last correction user wrote in bottom-left margin.
2. Look up latest NM week & number from embedded CSV.
3. Reply:
   - “Chart is current – no further NM needed.”
   - OR “Apply NM 6123/24 (week 22/24) and NM 6130/24 (week 23/24).”
4. Remind: “Enter date & NM number in pencil after pasting.”
5. If chart not in table → “Check Admiralty Notices to Mariners website.”