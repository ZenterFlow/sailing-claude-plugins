---
name: cross-track-error-monitor
description: Calculate and monitor Cross-Track Error (XTE) to maintain safe passage within Traffic Separation Schemes and narrow channels.
license: CC-BY-SA
---

# SKILL: cross-track-error-monitor
**RYA Yachtmaster – Cross-Track Error Monitoring**

## Purpose
Calculate Cross-Track Error (XTE) - the perpendicular distance from vessel's actual position to the intended track. Essential for TSS (Traffic Separation Scheme) navigation, narrow channels, and passage monitoring. Warns when exceeding safe limits.

## Activation Triggers
- "cross track error"
- "XTE"
- "how far off track"
- "distance from track"
- "TSS navigation"
- "am I in my lane"
- "track deviation"

## Behaviour
1. Ask user for:
   - Planned track (course line in degrees True)
   - Current position (from GPS or fix)
   - Original start position or waypoint
   - Safe XTE limit (if in TSS or channel)

2. Calculate XTE step-by-step:
   - Distance along track from start point
   - Perpendicular distance from track line
   - Direction of error (port or starboard of track)
   - XTE value in nautical miles or meters

3. Assessment and Warnings:

   **For TSS/Channels**:
   - **SAFE** (<0.1 nm / 200m): Well within lane
   - **CAUTION** (0.1-0.2 nm / 200-400m): Approaching limit
   - **WARNING** (0.2-0.3 nm / 400-600m): Near lane edge
   - **DANGER** (>0.3 nm / >600m): Exiting lane - IMMEDIATE ACTION

   **For Coastal Navigation**:
   - **GOOD** (<0.25 nm): Minor deviation
   - **ACCEPTABLE** (0.25-0.5 nm): Normal for coastal
   - **MONITOR** (0.5-1.0 nm): Check conditions
   - **CONCERN** (>1.0 nm): Investigate cause

4. Provide Corrections:
   - Course correction needed to regain track
   - New course to steer (accounting for current set)
   - Estimated time to return to track
   - Parallel track option if safer

5. Teaching Points:
   - XTE grows with time if not corrected
   - Small errors early are easier to fix than large errors late
   - In TSS: must stay within lane boundaries (typically 1-2 nm wide)
   - Monitor XTE continuously in restricted waters
   - GPS/chartplotter shows XTE automatically, but verify manually

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor-level briefing
- `resources/tss-requirements.md` – TSS lane widths and regulations
- `resources/xte-calculations.md` – Mathematical methods
- `templates/xte-worked-example.md` – Complete calculation
- `tests/sample-prompts.md` – 5 validation prompts

## Example Session
User: "I'm in Dover Strait TSS northbound lane. Planned track is 045°T from 51°00'N 001°30'E. My current position is 51°10'N 001°45'E. Am I safe?"

Skill returns:
```
CROSS-TRACK ERROR ANALYSIS
═══════════════════════════════════════

LOCATION: Dover Strait TSS (Northbound)
PLANNED TRACK: 045°T
START POSITION: 51°00.0'N, 001°30.0'E
CURRENT POSITION: 51°10.0'N, 001°45.0'E

CALCULATION:
─────────────────────────────────────
Distance along track: 14.2 nm
Distance from track: 0.15 nm (300m)
Direction: STARBOARD of planned track

CROSS-TRACK ERROR (XTE)
═══════════════════════════════════════
XTE = 0.15 nm (300 meters) to STARBOARD

TSS STATUS: ⚠ CAUTION
─────────────────────────────────────
✓ Still within northbound lane
⚠ Approaching lane edge (lane width ~1.5nm)
⚠ Current XTE: 300m (~20% of lane width used)

RECOMMENDATIONS:
────────────────────────────────────
→ Adjust course 3-5° to PORT
→ Monitor XTE every 10 minutes
→ Target: Return to centerline within 2 nm
→ Do NOT cross into southbound lane
→ Check for traffic on port side

CORRECTION COURSE:
────────────────────────────────────
Current track: ~052°T (drifting starboard)
Recommended: Steer 040-042°T to regain track
Monitor and adjust as XTE decreases

⚠ MAINTAIN TRAFFIC WATCH
TSS regulations require:
→ Stay within lane
→ Follow traffic direction (045°T)
→ Avoid crossing lanes
→ Monitor VHF Ch 16 and local traffic
```

## Teaching Notes
- XTE is perpendicular (shortest) distance to track
- Not the same as distance from waypoint
- Modern GPS shows XTE automatically - verify it makes sense
- In TSS: lane width typically 1-2 nm, stay within it
- Small corrections early prevent large problems later
- Wind/stream cause XTE - monitor and adjust continuously

## Common Student Errors
1. Confusing XTE with distance to waypoint (not the same!)
2. Not recognizing which side of track (port/starboard)
3. Ignoring small XTE until it becomes large
4. Over-correcting (creates oscillation)
5. Not accounting for continuing set/drift

## Version
v1.0.0 (2025-11-09)
