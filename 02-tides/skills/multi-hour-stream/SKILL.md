---
name: multi-hour-stream
description: Integrates multiple hourly tidal stream vectors into single resultant for passage planning and EP calculations.
license: CC-BY-SA
---

# SKILL: multi-hour-stream
**RYA Yachtmaster – Multi-Hour Tidal Stream Integration**

## Purpose
Combine multiple sequential hourly tidal vectors into a single resultant vector for long passage planning and estimated position calculations. This method reduces chart clutter, improves accuracy over multi-hour transits, and follows best practice for passage planning.

## Activation Triggers
- "integrate tidal streams"
- "multiple hour tide"
- "combine tidal vectors"
- "resultant tidal stream"
- "long passage tide calculation"
- "EP with multiple hours"

## Behaviour
1. Ask user for:
   - Trip duration (or ETA)
   - Start time (or departure time)
   - Boat speed
   - List of hourly tidal streams (direction & rate) OR
   - Almanac reference to extract stream data

2. Break down the passage:
   - Identify each hour (or partial hour) of transit
   - Determine tidal hour offset from HW for each segment
   - Extract or request direction and rate for each hour
   - Calculate distance for each tidal vector (rate × time)

3. Perform vector integration:
   - Describe graphical method (vectors tip-to-tail)
   - OR perform mathematical vector addition
   - Calculate resultant direction (True)
   - Calculate resultant distance (nautical miles)
   - Show all intermediate steps

4. Handle partial hours:
   - Calculate proportional distance: rate × (minutes/60)
   - Include in vector chain
   - Show arithmetic clearly

5. Present results:
   - Single resultant tidal vector (direction & distance)
   - Or express as: direction & equivalent rate over passage duration
   - Explain how to apply to chart (from departure or from fix)
   - Compare to plotting each hour separately (time saved)

6. Provide worked example with:
   - Clear vector diagram description (or ASCII art)
   - Step-by-step vector addition
   - Verification checks
   - Application to course to steer or EP

7. Warnings:
   - All directions must be True (convert from Magnetic if needed)
   - All tidal hours referenced to same HW time
   - Assumes straight-line ground track
   - Less accurate in areas with rapidly changing streams
   - Should verify with fixes when available

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full vector integration method and formulas
- `resources/` – vector addition guides, trigonometry references
- `templates/` – worked multi-hour integration examples
- `tests/sample-prompts.md` – 7 validation prompts

## Example Session
User: "I'm sailing from position A to B, will take about 3.5 hours at 6 knots. Tides are: HW+1: 2.0kn at 090°T, HW+2: 2.3kn at 095°T, HW+3: 2.5kn at 100°T, HW+4: 2.2kn at 105°T (partial). What's the integrated tidal vector?"

Skill:
```
Multi-Hour Tidal Stream Integration

Passage duration: 3.5 hours
Breakdown:
- Hour 1 (HW+1): 2.0 knots at 090°T for 1.0 hour = 2.0 NM at 090°T
- Hour 2 (HW+2): 2.3 knots at 095°T for 1.0 hour = 2.3 NM at 095°T
- Hour 3 (HW+3): 2.5 knots at 100°T for 1.0 hour = 2.5 NM at 100°T
- Hour 4 (HW+4): 2.2 knots at 105°T for 0.5 hour = 1.1 NM at 105°T

Vector Integration (mathematical method):

Convert each vector to Cartesian components:
Vector 1: 2.0 NM at 090°T
  North: 2.0 × cos(90°) = 0.00 NM
  East:  2.0 × sin(90°) = 2.00 NM

Vector 2: 2.3 NM at 095°T
  North: 2.3 × cos(95°) = -0.20 NM
  East:  2.3 × sin(95°) = 2.29 NM

Vector 3: 2.5 NM at 100°T
  North: 2.5 × cos(100°) = -0.43 NM
  East:  2.5 × sin(100°) = 2.46 NM

Vector 4: 1.1 NM at 105°T
  North: 1.1 × cos(105°) = -0.28 NM
  East:  1.1 × sin(105°) = 1.06 NM

Sum components:
  Total North: 0.00 + (-0.20) + (-0.43) + (-0.28) = -0.91 NM
  Total East:  2.00 + 2.29 + 2.46 + 1.06 = 7.81 NM

Calculate resultant:
  Distance = √((-0.91)² + (7.81)²)
           = √(0.83 + 61.00)
           = √61.83
           = 7.9 NM

  Direction = arctan(East / North)
            = arctan(7.81 / -0.91)
            = 096°T

Answer:
- Resultant tidal vector: 7.9 NM at 096°T
- Equivalent rate: 7.9 NM / 3.5 hours = 2.3 knots at 096°T

Application:
For COURSE TO STEER: Plot this single vector from your departure point
For EP: Plot this single vector from your last fix

This saves plotting 4 separate hourly vectors on the chart and gives
more accurate result for the overall passage.

Graphical interpretation:
On paper, you would draw:
1. Vector 1: 2.0 NM at 090° from origin
2. Vector 2: 2.3 NM at 095° from tip of vector 1
3. Vector 3: 2.5 NM at 100° from tip of vector 2
4. Vector 4: 1.1 NM at 105° from tip of vector 3
5. Resultant: Draw from origin to final tip
6. Measure: 7.9 NM at 096°T
```
