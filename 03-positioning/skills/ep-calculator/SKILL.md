---
name: ep-calculator
description: Calculate Estimated Position (EP) and Dead Reckoning (DR) accounting for leeway, tidal stream, and course/speed errors.
license: CC-BY-SA
---

# SKILL: ep-calculator
**RYA Yachtmaster – Estimated Position & Dead Reckoning**

## Purpose
Calculate Estimated Position (EP) by applying leeway and tidal stream to a known position. Distinguish between Dead Reckoning (DR - course and speed only) and EP (DR + environmental factors). Essential for navigation when visual fixes unavailable.

## Activation Triggers
- "estimated position"
- "calculate EP"
- "dead reckoning"
- "DR position"
- "position with leeway"
- "account for tidal stream"
- "where am I now"
- "plot EP"

## Behaviour
1. Ask user for:
   - Last known position (fix with time)
   - Course steered (compass or true)
   - Speed through water (or log reading)
   - Time elapsed (or current time)
   - Wind direction (for leeway estimate)
   - Leeway angle (or estimate from conditions)
   - Tidal stream set and drift (from diamonds or atlas)

2. Calculate in sequence (show each step):

   **Step A: Dead Reckoning (DR)**
   - Distance = Speed × Time
   - Plot from last position along course steered
   - This is DR position (no environmental factors)

   **Step B: Apply Leeway**
   - Leeway direction: downwind of course steered
   - Typical values: 5-10° (cruising yacht), 10-15° (light air), 2-5° (heavy weather)
   - Adjust course line by leeway angle
   - Plot Water Track (WT)

   **Step C: Apply Tidal Stream**
   - From water track endpoint, plot tidal vector
   - Set (direction of stream) and drift (speed × time)
   - This gives Estimated Position (EP)

3. Mark positions clearly:
   - **Fix**: Circle with time (⊙ 10:00)
   - **DR**: Single triangle with time (△ 10:30 DR)
   - **EP**: Double triangle with time (▽▽ 10:30 EP)

4. Quality Assessment:
   - **HIGH CONFIDENCE**: Recent fix (<1 hour), accurate log, known stream
   - **MEDIUM CONFIDENCE**: Fix 1-3 hours old, estimated leeway
   - **LOW CONFIDENCE**: Fix >3 hours old, uncertain stream, variable conditions
   - **GET NEW FIX**: EP >4 hours old, entering hazards, or poor visibility

5. Teaching Points:
   - DR = course + speed only (what your instruments show)
   - EP = DR + leeway + stream (where you actually are)
   - Always update EP when you get a new fix
   - EP uncertainty grows with time
   - Leeway is TO LEEWARD (downwind) of heading

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor-level briefing
- `resources/leeway-estimates.md` – typical leeway values by conditions
- `resources/ep-vs-dr.md` – comparison and when to use each
- `templates/ep-worked-example.md` – complete calculation
- `templates/ep-quick-plot.md` – simplified plotting guide
- `tests/sample-prompts.md` – 5 validation prompts

## Example Session
User: "Last fix at 09:00 was 50°30'N 002°00'W. I've been steering 090°C at 5 knots. It's now 11:00. Wind from SW, moderate breeze. Tidal stream 135°T at 1.5 knots. Deviation 3°W, Variation 5°W."

Skill returns:
```
ESTIMATED POSITION CALCULATION
═══════════════════════════════════════

LAST KNOWN POSITION (FIX)
⊙ 09:00 – 50°30.0'N, 002°00.0'W

TIME ELAPSED: 2 hours

STEP 1: DEAD RECKONING (DR)
─────────────────────────────────────
Course Steered: 090°C - 3° (dev) - 5° (var) = 082°T
Speed: 5.0 knots
Distance: 5 kts × 2 hrs = 10.0 nm

DR Position (no leeway/stream):
△ 11:00 DR – 50°30.0'N, 001°40.5'W

STEP 2: APPLY LEEWAY
─────────────────────────────────────
Wind: SW (225°) → Leeway to NE (starboard tack)
Conditions: Moderate breeze, cruising yacht
Leeway estimate: 7° to leeward (downwind)

Water Track: 082°T + 7° = 089°T
Distance: 10.0 nm (same as DR distance)

Position after leeway:
50°30.0'N, 001°40.2'W

STEP 3: APPLY TIDAL STREAM
─────────────────────────────────────
Set: 135°T (SE)
Drift: 1.5 kts × 2 hrs = 3.0 nm

From water track position, plot:
→ 135°T for 3.0 nm

ESTIMATED POSITION (EP)
═══════════════════════════════════════
▽▽ 11:00 EP – 50°27.5'N, 001°38.8'W

CONFIDENCE: MEDIUM
✓ Fix is 2 hours old (acceptable)
✓ Tidal stream known from chart
⚠ Leeway estimated (not measured)

RECOMMENDATIONS:
→ Update with visual fix when possible
→ Check depth sounder matches charted depth
→ If entering confined waters: GET NEW FIX
→ Maximum EP age before new fix: 3-4 hours

VECTOR SUMMARY:
────────────────────────────────────
Fix 09:00          → DR (course/speed)
DR 11:00           → Leeway (7° starboard)
Water Track 11:00  → Stream (135°T, 3.0 nm)
EP 11:00           ✓ FINAL POSITION
```

## Teaching Notes
- **DR shows where instruments think you are**
- **EP shows where you actually are (probably)**
- EP is an ESTIMATE - uncertainty increases with time
- Always get new fix before entering hazards
- Check EP against depth soundings, transits, or clearing bearings
- If EP and fix differ significantly: check for current set, leeway error, or log error
- Plot both DR and EP - DR helps identify errors

## Common Student Errors
1. Forgetting to apply leeway TO LEEWARD (downwind)
2. Applying stream in wrong direction
3. Confusing course steered vs course made good
4. Not updating EP when new fix obtained
5. Over-confidence in old EP (>3 hours)
6. Plotting leeway upwind instead of downwind

## Version
v1.0.0 (2025-11-09)
