---
name: velocity-triangle-plotter
description: Plot and solve velocity triangles (water triangles) graphically for Course To Steer and Track Made Good problems.
license: CC-BY-SA
---

# SKILL: velocity-triangle-plotter
**RYA Yachtmaster – Velocity Triangle Plotting**

## Purpose
Graphically plot velocity (water) triangles to solve CTS and TMG problems. Visual method for understanding relationship between heading, water track, tidal stream, and track made good. Essential for chart work and exam plotting.

## Activation Triggers
- "velocity triangle"
- "water triangle"
- "plot vectors"
- "graphical CTS"
- "draw triangle"
- "vector diagram"
- "show me the triangle"

## Behaviour
1. Ask user for scenario type:
   - **Planning (CTS)**: Know desired track, need course to steer
   - **Plotting (TMG)**: Know course steered, need track made good

2. Gather required data:
   - Boat speed through water
   - Tidal stream set and drift
   - Leeway (if applicable)
   - Start/end positions or track direction

3. Create step-by-step graphical solution:

   **For CTS (Planning)**:
   ```
   1. Mark start position
   2. Draw desired track line from start
   3. From endpoint (1 hour ahead), plot tidal vector BACKWARDS
   4. From start, draw arc of boat speed radius
   5. Intersection shows water track
   6. Apply leeway to get heading
   7. Measure and label all vectors
   ```

   **For TMG (Plotting)**:
   ```
   1. Mark start position
   2. Draw heading line
   3. Apply leeway → water track
   4. Plot boat speed along water track (1 hour distance)
   5. From endpoint, plot tidal vector FORWARDS
   6. Result shows track made good
   7. Measure and label
   ```

4. Provide ASCII or text diagram showing:
   - All vectors with labels
   - Angles marked
   - Distances marked
   - Clear annotations

5. Explain each vector:
   - **Heading**: Direction vessel points
   - **Leeway**: Sideways drift from wind
   - **Water Track**: Course through water
   - **Boat Speed**: Speed through water
   - **Tidal Stream**: Water movement (set/drift)
   - **Track Made Good**: Actual path over ground
   - **Speed Over Ground**: Actual speed over ground

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full plotting instructions
- `resources/vector-diagrams.md` – Example diagrams
- `templates/triangle-plot.md` – Plotting template
- `tests/sample-prompts.md` – 5 validation prompts

## Example Session
User: "Show me the velocity triangle for: desired track 090°T, boat speed 5 kts, stream 180°T at 2 kts. No leeway."

Skill returns:
```
VELOCITY TRIANGLE - CTS PROBLEM
═══════════════════════════════════════

GIVEN:
• Desired Track Made Good (TMG): 090°T (East)
• Boat Speed: 5.0 knots
• Tidal Stream: 180°T @ 2.0 knots (South)
• Leeway: 0° (no wind effect)

GRAPHICAL SOLUTION:
─────────────────────────────────────

STEP 1: Mark start position (A)

STEP 2: Draw desired track 090°T from A
        A ───────────→ Track 090°T (East)

STEP 3: Mark point B at 5nm along track (1 hour at 5 kts SOG est.)

STEP 4: From B, plot tidal vector BACKWARDS
        (Stream is 180°T, so plot 000°T for 2 nm)

                C
                ↑ 2nm
                │ (000°T)
        A ──────┴────→ B
          5nm  090°T

STEP 5: From A, draw arc radius 5 nm (boat speed)
        Intersection with line from B shows water track endpoint C

STEP 6: Measure heading from A to C

VELOCITY TRIANGLE:
─────────────────────────────────────

              C (water track endpoint)
             /│\
            / │ \
     5nm   /  │  \ 2nm
    (boat /   │   \ (tidal vector)
    speed)    │    \
         /    │     \
        /     │      \
       /      │       \
      A ──────┴────────→ B
        Track 090°T (TMG)
           ~3.5nm SOG

MEASUREMENTS:
─────────────────────────────────────
AC (Water Track/Heading): 063°T, 5.0 nm
CB (Tidal Vector): 180°T @ 2.0 kts
AB (Track Made Good): 090°T, ~3.5 nm

SOLUTION:
═══════════════════════════════════════
COURSE TO STEER: 063°T (or 063°C after variation/deviation)
SPEED OVER GROUND: 3.5 knots
ETA for 10nm: 10 ÷ 3.5 = 2.9 hours (~2h 50m)

EXPLANATION:
─────────────────────────────────────
To make good 090°T (East):
→ Steer 063°T (NNE) through water
→ Southward stream pushes you south
→ Net result: move East as desired
→ But slower SOG (3.5 vs 5 kts) due to stream angle

⚠ Stream reduces effective speed significantly
```

## Teaching Notes
- Velocity triangle shows ALL vectors in one diagram
- Vectors must form closed triangle (or diagram is wrong)
- Can solve graphically on chart or mathematically
- Graphical method catches errors - if diagram looks wrong, it probably is
- Triangle shows why "steering into stream" is necessary

## Common Student Errors
1. Tidal vector wrong direction (forwards vs backwards)
2. Boat speed vs SOG confusion
3. Triangle doesn't close (calculation error)
4. Forgetting leeway vector
5. Mixing up which vector is which

## Version
v1.0.0 (2025-11-09)
