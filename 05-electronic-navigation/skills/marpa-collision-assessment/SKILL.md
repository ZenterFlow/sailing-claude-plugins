---
name: marpa-collision-assessment
description: MARPA target tracking, CPA/TCPA interpretation, and collision assessment.
license: CC-BY-SA
---

# SKILL: marpa-collision-assessment
**RYA Yachtmaster – MARPA Target Tracking and Collision Assessment**

## Purpose
Use Mini Automatic Radar Plotting Aid to track targets, interpret CPA/TCPA data, and assess collision risk with understanding of limitations.

## Activation Triggers
- "what is MARPA"
- "CPA TCPA"
- "radar target tracking"
- "collision assessment radar"

## Behaviour
**MARPA Operation**:

**Target Acquisition**:
1. Select target on radar screen (cursor)
2. System highlights with box
3. MARPA tracks relative motion
4. Requires several sweeps to establish track (1-3 minutes)

**Data Provided**:
- **CPA**: Closest Point of Approach (distance)
- **TCPA**: Time to CPA (minutes)
- Target course/speed (relative and true)
- Bearing/range (continuously updated)

**MARPA vs ARPA**:
- **MARPA**: "Mini" version for small craft
- **ARPA**: Full version on commercial ships
- MARPA limitations: Less processing power, fewer targets, simpler algorithms
- Both provide CPA/TCPA data

**CPA/TCPA Interpretation**:
- **Safe**: CPA > safe distance (typically > 1 NM)
- **Dangerous**: CPA < safe distance
- **Action needed**: TCPA < 15 minutes → immediate assessment
- **Critical**: CPA = 0.0 NM → collision course!

**Reliability Issues** ⚠️:
- **During target maneuver**: CPA/TCPA constantly changing
- Example: Vessel turning → unreliable while turning
- **Solution**: Wait for steady course before trusting data
- **Own ship maneuver**: Also affects reliability

**Collision Avoidance Workflow**:
1. Establish safe passing distance
2. Monitor CPA/TCPA for developing risks
3. Use MARPA to assess avoidance maneuver effectiveness
4. **Critical**: Don't rely solely on MARPA - maintain visual watch!

**MARPA Limitations**:
❌ Only tracks radar targets
❌ Unreliable during maneuvers
❌ Requires time to establish track
❌ Can't see non-radar-reflective targets
✅ Must combine with visual lookout

**Critical Teaching Point**:
"MARPA shows what's happening IF everyone maintains course and speed. Any maneuver invalidates the prediction."

## Version
v1.0.0 (2025-11-10)
