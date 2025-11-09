# SKILL: Computation of Rates Graph Application

## Description
Use the computation of rates graph to determine accurate tidal stream rates when range is between spring and neap values.

## Prerequisites
- SKILL_31 (Tidal Stream Usage)

## Learning Objectives
- Plot spring and neap rates on graph axes
- Draw rate interpolation line
- Find rate for given tidal range
- Extend line for ranges beyond spring/neap extremes
- Apply to both diamond and atlas data

## Graphical Method
**Setup:**
1. Calculate range: HW height - LW height (at reference port)
2. Locate spring rate on red dotted line (right axis)
3. Locate neap rate on blue dotted line (left axis)

**Plotting:**
1. Draw straight line connecting spring and neap points
2. Extend line beyond both dotted lines if needed
3. Find range value on horizontal axis
4. Draw vertical line to intersect your rate line
5. Draw horizontal to rate axis to read rate (tenths of knot)

**Example:**
- Range = 4.2m (between MHWN 3.5m and MHWS 5.0m)
- Spring rate = 2.3 knots
- Neap rate = 1.1 knots
- Result = 2.0 knots (interpolated)

**Extreme Ranges:**
- Range &gt; MHWS: Extend line beyond spring point
- Range &lt; MHWN: Extend line beyond neap point

## Common Errors
- Swapping spring and neap positions on graph
- Not extending line for extreme ranges
- Using wrong reference port range
- Reading scale incorrectly (tenths vs whole knots)

## Assessment
- Determine rate for 5 scenarios with ±0.1 kn accuracy
- Handle 2 cases requiring line extension
- Complete within 4 minutes per calculation