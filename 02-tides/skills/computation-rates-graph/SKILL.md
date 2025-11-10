---
name: computation-rates-graph
description: Uses the computation of rates graph to interpolate tidal stream rates between spring and neap values for actual range.
license: CC-BY-SA
---

# SKILL: computation-rates-graph
**RYA Yachtmaster – Computation of Rates Graph Application**

## Purpose
Accurately determine tidal stream rates when the actual tidal range falls between spring and neap extremes. Uses the graphical interpolation method found in Admiralty Tidal Stream Atlases and nautical almanacs to calculate precise rates for passage planning and estimated position calculations.

## Activation Triggers
- "computation of rates"
- "interpolate tidal stream"
- "tidal range is between spring and neap"
- "calculate stream rate for range"
- "use rates graph"
- "spring rate 2.3 neap rate 1.1"

## Behaviour
1. Ask user for:
   - Spring tidal stream rate (knots)
   - Neap tidal stream rate (knots)
   - Actual tidal range at reference port (meters)
   - Optional: MHWS, MHWN values for context

2. Explain the graphical method step-by-step:
   - Describe plotting spring rate on right (red dotted) axis
   - Describe plotting neap rate on left (blue dotted) axis
   - Explain drawing interpolation line between the two points
   - Show finding actual range on horizontal axis
   - Demonstrate reading interpolated rate

3. Calculate interpolated rate:
   - Use linear interpolation formula if graph not available
   - Show arithmetic clearly
   - Round to nearest 0.1 knot (standard precision)
   - Apply to tidal stream direction from almanac/chart

4. Provide worked example with:
   - Visual description of graph plotting
   - Step-by-step calculation
   - Final rate with direction
   - Units clearly stated

5. Warnings:
   - Verify correct reference port used for range
   - Flag if range exceeds MHWS (extrapolation needed)
   - Flag if range below MHWN (extrapolation needed)
   - Note that direction doesn't change, only rate

6. For extreme ranges:
   - Explain line extension beyond spring or neap points
   - Caution about accuracy of extrapolation
   - Suggest checking actual conditions vs predictions

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full graphical method and interpolation formulas
- `resources/` – graph examples, range tables
- `templates/` – worked interpolation examples
- `tests/sample-prompts.md` – 7 validation prompts

## Example Session
User: "Spring rate is 2.3 knots, neap rate is 1.1 knots. Current range at reference port is 4.2m. MHWS=5.0m, MHWN=3.5m. What's the actual rate?"

Skill:
```
Computation of Rates Graph Method:

Given data:
- Spring rate: 2.3 knots (plotted on right/red axis)
- Neap rate: 1.1 knots (plotted on left/blue axis)
- Actual range: 4.2m
- MHWS: 5.0m, MHWN: 3.5m

Step 1: Position range on scale
Range 4.2m is between MHWN (3.5m) and MHWS (5.0m)
Range span = 5.0 - 3.5 = 1.5m
Position = (4.2 - 3.5) / 1.5 = 0.7 / 1.5 = 0.47 (47% from neap to spring)

Step 2: Interpolate rate
Rate range = 2.3 - 1.1 = 1.2 knots
Interpolated increase = 1.2 × 0.47 = 0.56 knots
Interpolated rate = 1.1 + 0.56 = 1.66 knots

Step 3: Round to standard precision
Answer: 1.7 knots

Graphical interpretation:
On the computation of rates graph, you would:
- Plot 2.3 on the right (spring/red) axis
- Plot 1.1 on the left (neap/blue) axis
- Draw a straight line connecting these points
- Find 4.2m on the horizontal axis
- Read up to the line, across to rate axis
- Read approximately 1.7 knots

Use this rate with the stream direction from the tidal diamond/atlas.
```
