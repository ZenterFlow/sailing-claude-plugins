---
name: ais-target-interpretation
description: Interpret AIS target symbols, data, and collision assessment (CPA/TCPA).
license: CC-BY-SA
---

# SKILL: ais-target-interpretation
**RYA Yachtmaster – AIS Target Interpretation**

## Purpose
Interpret AIS target symbols and data, assess collision risk using CPA/TCPA, and understand AIS limitations.

## Activation Triggers
- "what is AIS"
- "AIS target symbols"
- "CPA and TCPA"
- "AIS collision assessment"

## Behaviour
**AIS (Automatic Identification System)**:
- Broadcasts vessel info: Name, MMSI, position, COG, SOG, heading
- Receives broadcasts from other AIS-equipped vessels
- Updates every few seconds
- Range: Typically 20-30 NM (VHF radio range)

**AIS Target Symbols**:
- **Triangle**: Active AIS target, moving
- **Arrow direction**: Target's heading
- **Vector line**: Track over ground (COG/SOG)
- **Activated target**: Selected for detailed info
- **Sleeping target**: Not selected, displayed simply

**Key AIS Data Fields**:
- **Name & MMSI**: Vessel identification
- **COG**: Course Over Ground (direction of travel)
- **SOG**: Speed Over Ground
- **Heading**: Direction vessel is pointing (may differ from COG)
- **CPA**: Closest Point of Approach (distance)
- **TCPA**: Time to Closest Point of Approach

**CPA/TCPA Collision Assessment**:
- **CPA < 0.5 NM**: Potential collision risk
- **TCPA < 20 min**: Action may be required soon
- **CPA = 0.0 NM**: Collision course!
- **TCPA negative**: Target has passed CPA

**Critical Limitations**:
❌ Only shows vessels WITH transmitting AIS
❌ Small craft may not have AIS
❌ CPA/TCPA unreliable during target maneuvers
❌ Not all vessels use AIS (fishing boats, military)
❌ **Must maintain visual watch** - AIS is aid only!

**Integration with Radar**:
- **Radar**: Detects all targets (including non-AIS)
- **AIS**: Identifies targets with full info
- **Best practice**: Use BOTH for complete picture
- Radar + AIS = comprehensive collision avoidance

**AIS for Navigation**:
- Identify vessels ahead in TSS lanes
- Monitor large ship movements near harbor
- Communicate via VHF using MMSI/name
- Track ferry/commercial routes

**Critical Teaching Point**:
"AIS shows you what's transmitting. Radar shows you what's there. Use both."

## Version
v1.0.0 (2025-11-10)
