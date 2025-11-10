---
name: harbor-entry-planner
description: Create comprehensive harbor entry plans with approach procedures, abort criteria, and contingency planning.
license: CC-BY-SA
---

# SKILL: harbor-entry-planner
**RYA Yachtmaster – Harbor Entry Planning**

## Purpose
Create detailed harbor entry plans covering approach procedures, clearing bearings, leading lines, depth checks, abort criteria, and contingencies. Implements "Plan A, B, C + abort criteria" methodology for safe harbor approaches.

## Activation Triggers
- "harbor entry plan"
- "approach plan"
- "harbor approach"
- "pilotage plan"
- "entry procedure"
- "abort criteria"

## Behaviour
1. **Gather information**:
   - Harbor name and entry position
   - Vessel draught and beam
   - Weather and tide conditions
   - Available charts and pilot books

2. **Create comprehensive plan**:

   **A. Approach Phase**:
   - Initial position (waypoint or fix position)
   - Approach track and CTS
   - Key position checks (clearing bearings, transits, depth contours)
   - Speed and timing

   **B. Entry Phase**:
   - Entry point identification
   - Leading lines or range markers
   - Depth checks and clearances
   - Traffic and VHF protocols
   - Final approach track

   **C. Abort Criteria** (Define BEFORE starting):
   - Weather limits (wind, visibility, sea state)
   - Tidal limits (minimum depth, stream limits)
   - Navigation limits (if clearing bearing exceeded, if transit lost)
   - Traffic conflicts
   - Equipment failures

   **D. Plan B & C**:
   - Alternative entry time (next tide, daylight)
   - Alternative harbor
   - Anchoring outside if entry unsafe
   - Heaving-to offshore

3. **Safety checks**:
   - Chart currency verified
   - Tidal heights calculated
   - Weather forecast reviewed
   - Crew briefed
   - Emergency contacts logged

## Example Output
```
HARBOR ENTRY PLAN: DARTMOUTH
═══════════════════════════════════════

VESSEL: Example Yacht, Draught 1.8m
CONDITIONS: Wind SW F4, Tide HW-2, Visibility good

PLAN A: STANDARD ENTRY
─────────────────────────────────────
1. Initial Position: 50°19.5'N, 003°33.0'W (2nm SE of entrance)
2. Approach: Track 315°T at 4 knots
3. Clearing Bearings:
   • Keep Dartmouth Castle NMT 340°T (clears Black Rock)
   • Keep Start Point NLT 110°T (clears Homestone)
4. Entry: Follow leading line (castle tower/church) 350°T
5. Depth: Maintain >5m (3.2m charted + 1.5m tide + 0.3m safety)
6. VHF: Monitor Ch 11 Dartmouth Harbor

ABORT CRITERIA:
⛔ Wind >F5 or visibility <1nm
⛔ Depth <4m at any point
⛔ Clearing bearing limit reached
⛔ Cannot identify leading marks

PLAN B: Delay entry, anchor in Start Bay
PLAN C: Proceed to Brixham (alternative harbor)

CREW BRIEF: All hands on deck, fenders port side, lines ready
```

## Version
v1.0.0 (2025-11-09)
