---
name: clearing-bearing-calculator
description: Calculate clearing bearings (danger bearings) using NMT and NLT rules to safely avoid hazards during harbor approaches.
license: CC-BY-SA
---

# SKILL: clearing-bearing-calculator
**RYA Yachtmaster – Clearing Bearings & Danger Bearings**

## Purpose
Calculate clearing bearings (danger bearings) to ensure safe passage clear of rocks, shoals, and hazards during harbor approaches and coastal pilotage. Uses NMT (No More Than) and NLT (No Less Than) rules to define safe water boundaries.

## Activation Triggers
- "clearing bearing"
- "danger bearing"
- "NMT bearing"
- "NLT bearing"
- "no more than"
- "no less than"
- "safe bearing"
- "hazard avoidance bearing"

## Behaviour
1. Ask user for:
   - Hazard location (position or charted object)
   - Safe water area (where vessel should stay)
   - Reference object for bearing (lighthouse, headland, etc.)
   - Optional: vessel position for verification

2. Calculate clearing bearing step-by-step:

   **Determine bearing type needed**:
   - **NMT (No More Than)**: Maximum safe bearing - stay BELOW this bearing
   - **NLT (No Less Than)**: Minimum safe bearing - stay ABOVE this bearing

   **Calculate the bearing**:
   - Measure bearing from vessel to reference object
   - Determine which side of bearing line is safe
   - State rule clearly: "Keep bearing to [object] NMT XXX°" or "NLT XXX°"

3. Provide visual explanation:
   ```
   HAZARD (rocks/shoal)
        │
        │ Danger bearing line
        │
        ├─────── Reference Object
        │
   SAFE WATER
   ```

4. Safety checks and warnings:
   - **Color-coded status**:
     - ✅ SAFE: Bearing within safe limits
     - ⚠️ CAUTION: Approaching clearing bearing limit
     - ⛔ DANGER: Bearing outside safe limits - hazard risk

   - Verify bearing makes sense (check chart)
   - Remind to apply variation and deviation
   - Note that clearing bearing is compass bearing to steer by
   - Recommend frequent bearing checks (every 5-10 minutes)

5. Provide practical guidance:
   - How to monitor clearing bearing continuously
   - What to do if approaching limit
   - Alternative clearing bearings if available
   - Depth contour as backup safety check

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor-level briefing
- `resources/clearing-bearing-types.md` – NMT vs NLT explained
- `resources/hazard-avoidance-guide.md` – Practical application guide
- `templates/clearing-bearing-worked-example.md` – Complete scenario
- `tests/sample-prompts.md` – 5 validation prompts

## Example Session
User: "There's a rock at 50°20'N 004°10'W. I want to pass north of it. Reference object is Start Point lighthouse at 50°22'N 004°08'W. What clearing bearing should I use?"

Skill returns:
```
CLEARING BEARING CALCULATION
═══════════════════════════════════════

HAZARD: Rock at 50°20.0'N, 004°10.0'W
REFERENCE: Start Point Lighthouse (50°22.0'N, 004°08.0'W)
SAFE WATER: North side (staying north of rock)

STEP 1: MEASURE BEARING FROM ROCK TO REFERENCE
─────────────────────────────────────
Rock position: 50°20.0'N, 004°10.0'W
Lighthouse: 50°22.0'N, 004°08.0'W

Bearing from rock to lighthouse: 028°T (approx)

STEP 2: DETERMINE CLEARING BEARING TYPE
─────────────────────────────────────
Safe water: NORTH of rock
Rock-to-lighthouse bearing: 028°T

To stay NORTH (left) of this bearing line:
→ Vessel bearing to lighthouse must be LESS THAN 028°T

CLEARING BEARING RULE
═══════════════════════════════════════
Keep Start Point Lighthouse bearing:

  ⛔ NMT 028°T (No More Than)

INTERPRETATION:
─────────────────────────────────────
✅ SAFE: Bearing 000-027°T (north of danger line)
⚠️ CAUTION: Bearing 028°T (on danger line)
⛔ DANGER: Bearing 029-360°T (south of danger line - hazard risk)

VISUAL DIAGRAM:
─────────────────────────────────────
         028°T bearing line
              /
    SAFE     / Start Point
   (NORTH)  /  Lighthouse
           /
          /
    ⛔ ROCK
        \
         \  DANGER
          \ (SOUTH)

PRACTICAL USAGE:
─────────────────────────────────────
1. Take bearing to Start Point regularly (every 5-10 min)
2. ENSURE bearing stays BELOW 028°T
3. If bearing increases toward 028°T: Alter course to port
4. If bearing exceeds 028°T: IMMEDIATE action - turn port NOW

BACKUP CHECKS:
─────────────────────────────────────
→ Depth contour: Rock is in <10m water, stay in >15m
→ Visual check: Keep lighthouse left of beam
→ GPS: Monitor position on chart plotter

MAGNETIC CONVERSION (Example):
─────────────────────────────────────
True bearing: NMT 028°T
Variation: 5°W → subtract
Magnetic: NMT 023°M
Deviation: 2°W → subtract
COMPASS: Keep bearing NMT 021°C

⚠️ IMPORTANT: Apply your vessel's variation and deviation!
```

## Teaching Notes
- Clearing bearing is one line on chart that separates safe from dangerous water
- NMT = "No More Than" = maximum safe bearing (stay left/lower)
- NLT = "No Less Than" = minimum safe bearing (stay right/higher)
- Always verify which side of line is safe before defining rule
- Monitor continuously - clearing bearings are useless if not checked
- Combine with depth contours for redundancy

## Common Student Errors
1. Confusing NMT and NLT (getting the rule backwards)
2. Not applying variation/deviation to clearing bearing
3. Measuring bearing from wrong direction
4. Not checking frequently enough
5. Forgetting which side of bearing line is safe

## Version
v1.0.0 (2025-11-09)
