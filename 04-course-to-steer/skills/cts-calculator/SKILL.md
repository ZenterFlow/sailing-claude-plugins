---
name: cts-calculator
description: Calculate Course To Steer (CTS) accounting for leeway, tidal stream, and magnetic variation to achieve desired track.
license: CC-BY-SA
---

# SKILL: cts-calculator
**RYA Yachtmaster – Course To Steer Calculator**

## Purpose
Calculate what compass course to steer to achieve a desired track over ground, accounting for leeway from wind and tidal stream set/drift. Solves the "water triangle" problem for passage planning and navigation.

## Activation Triggers
- "course to steer"
- "CTS"
- "what course should I steer"
- "calculate CTS"
- "water triangle"
- "track 090 with stream"
- "account for tide and leeway"

## Behaviour
1. Ask user for:
   - Desired Track Made Good (TMG) in degrees True
   - Boat speed through water (knots)
   - Wind direction and estimated leeway (or estimate from conditions)
   - Tidal stream set (direction) and drift (speed)
   - Magnetic variation and compass deviation

2. Calculate using vector triangle method:

   **Step 1: Apply Tidal Stream (Reverse)**
   - From destination, plot RECIPROCAL of tidal set for tidal drift distance
   - This shows where vessel must be in water to be carried to destination by tide

   **Step 2: Calculate Water Track**
   - From start position to tide-corrected position
   - This is direction vessel must travel through water

   **Step 3: Apply Leeway**
   - Leeway is TO LEEWARD (downwind)
   - Adjust water track by leeway angle to get heading
   - Subtract leeway if wind on port
   - Add leeway if wind on starboard

   **Step 4: Convert to Compass Course**
   - True → Magnetic: subtract variation (if West)
   - Magnetic → Compass: subtract deviation (if West)
   - This is Course To Steer (CTS)

3. Provide complete solution showing:
   - Track Made Good (desired): XXX°T
   - Water track (after tide correction): XXX°T
   - Heading (after leeway): XXX°T
   - Course to Steer: XXX°C
   - Estimated speed over ground
   - ETA at destination

4. Validation checks:
   - If stream > boat speed: may not make desired track (warn)
   - If course change >30° from rhumb line: verify calculations
   - Show diagram of vector triangle

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor-level briefing
- `resources/cts-method.md` – Step-by-step calculation method
- `templates/cts-worked-example.md` – Complete example with diagram
- `tests/sample-prompts.md` – 5 validation prompts

## Example Session
User: "I want to make good a track of 090°T. Boat speed 5 knots. Stream is 180°T at 2 knots. Wind from North, leeway 6°. Variation 5°W, deviation 2°W. What course do I steer?"

Skill returns:
```
COURSE TO STEER CALCULATION
═══════════════════════════════════════

DESIRED TRACK MADE GOOD: 090°T (Due East)
BOAT SPEED: 5.0 knots
STREAM: 180°T at 2.0 knots (Southward)
LEEWAY: 6° (Wind from N, port tack)
VARIATION: 5°W
DEVIATION: 2°W

STEP 1: TIDAL STREAM CORRECTION
─────────────────────────────────────
Stream carries vessel 180°T (S) at 2 kts
To compensate: head MORE NORTH than 090°T

STEP 2: WATER TRACK (Vector Solution)
─────────────────────────────────────
Required track: 090°T
Stream effect: -2 kts southward
Water track needed: ~063°T
(To make 090°T over ground, steer NE through water)

STEP 3: APPLY LEEWAY
─────────────────────────────────────
Wind from North → pushed to SOUTH (port tack)
Leeway 6° to PORT
To compensate: steer MORE NORTH

Water track: 063°T
Leeway correction: -6° (subtract for port tack)
Heading required: 063° - 6° = 057°T

STEP 4: CONVERT TO COMPASS
─────────────────────────────────────
True heading: 057°T
Variation: 5°W → subtract
Magnetic: 057° - 5° = 052°M
Deviation: 2°W → subtract
Compass: 052° - 2° = 050°C

COURSE TO STEER (CTS)
═══════════════════════════════════════
🧭 STEER: 050°C

VALIDATION:
─────────────────────────────────────
✓ Heading 057°T through water
✓ Leeway 6° south → Water track 063°T
✓ Stream 2 kts south → Track Made Good 090°T
✓ Speed Over Ground: ~3.5 kts (reduced by southward stream)

SUMMARY VECTOR:
CTS 050°C → Heading 057°T → Water Track 063°T → TMG 090°T

TIME/DISTANCE:
─────────────────────────────────────
For 10 nm run at 090°T:
- Distance through water: ~11 nm
- Speed over ground: 3.5 kts
- ETA: 2 hours 50 minutes

⚠ Note: Strong southward stream reduces SOG significantly
```

## Teaching Notes
- CTS is REVERSE of EP: EP plots from past, CTS plans for future
- Vector order: Stream first (can't control), then leeway, then convert to compass
- If stream > boat speed: cannot make desired track (set by sideways)
- Always verify result makes sense (draw diagram)

## Common Student Errors
1. Applying stream in wrong direction (should plot AGAINST stream)
2. Adding leeway instead of subtracting (or vice versa)
3. Forgetting variation/deviation conversions
4. Not checking if solution is possible (stream too strong)

## Version
v1.0.0 (2025-11-09)
