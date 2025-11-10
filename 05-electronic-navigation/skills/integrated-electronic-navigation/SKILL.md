---
name: integrated-electronic-navigation
description: Use multiple electronic systems together for navigation with cross-verification.
license: CC-BY-SA
---

# SKILL: integrated-electronic-navigation
**RYA Yachtmaster – Integrated Electronic Navigation Systems**

## Purpose
Use multiple electronic systems (GPS, radar, AIS, depth, log) together for navigation, understanding each system's role and cross-verifying information.

## Activation Triggers
- "integrate electronic systems"
- "cross-check GPS position"
- "verify electronic navigation"
- "redundant navigation"

## Behaviour
**Primary Navigation Loop**:
1. GPS plotter → Primary position source
2. Radar ranges → Verify position on charted objects
3. Depth sounder → Verify position on depth contours
4. All agree → High confidence
5. Disagreement → Investigate and resolve

**Speed Analysis**:
- Log speed (water) vs SOG (ground) = Tide + Leeway effect
- Application: Identify tidal stream, estimate leeway magnitude
- Example: Log 5 kn, SOG 7 kn → 2 kn favorable tide

**Collision Avoidance Integration**:
1. **Radar**: Detect ALL objects (including non-AIS)
2. **AIS**: Identify vessel details, course, speed
3. **Visual**: Confirm and assess situation
4. **Integrated picture**: Best collision avoidance strategy

**Position Verification Methods**:
- GPS fix (primary)
- Radar range fix (2-3 charted objects)
- Depth contour (sounder matches expected)
- Visual fix (when objects visible)
- Running fix (single object, time interval)

**System Limitations Cross-Check**:
- GPS error → Check radar ranges, depth, visual
- Radar shadow → Use visual, GPS
- AIS not transmitting → Use radar, visual
- Depth false reading → Check GPS, deeper water

**Redundancy Principle**:
✅ Never rely on single system
✅ Always maintain paper chart plot
✅ Log positions regularly for DR/EP backup
✅ Know how to navigate if all electronics fail

**Critical Teaching Point**:
"Electronics provide information. Seamanship makes decisions."

## Version
v1.0.0 (2025-11-10)
