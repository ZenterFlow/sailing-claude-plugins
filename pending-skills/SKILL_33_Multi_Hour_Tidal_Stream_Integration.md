# SKILL: Multi-Hour Tidal Stream Integration

## Description
Combine multiple hourly tidal vectors into a single resultant vector for long passage planning and EP calculation.

## Prerequisites
- SKILL_31 (Tidal Stream Usage)
- SKILL_32 (Computation of Rates)

## Learning Objectives
- Plot sequential hourly tidal vectors on graph paper
- Vector-add tides to find resultant set and distance
- Apply partial hour calculations (time proportion)
- Use resultant tide for course to steer/EP
- Minimize chart wear by plotting once

## Integration Method
**Trip Analysis:**
1. Plot intended ground track on chart
2. Mark hourly intervals along track
3. Determine trip duration from speed/distance
4. Identify tidal hour(s) for each segment

**Hourly Tidal Vectors:**
For each hour (or partial hour):
- Determine hour offset from HW (e.g., HW+2, HW+3)
- Extract direction and rate (use computation of rates if needed)
- Calculate distance = rate × time fraction

**Graphical Addition:**
1. Draw first tidal vector from origin
2. Draw second vector from first vector's tip
3. Continue for all hours in sequence
4. Draw resultant from origin to final tip
5. Measure direction and total distance

**Partial Hours:**
- Rate × (minutes/60) = distance for that segment
- Example: 0.3 knots × 50/60 = 0.25 NM

**Application:**
- Use single resultant tide vector on chart
- Plot from departure point for course to steer
- Plot from fix for estimated position
- Saves multiple markings on chart

## Common Errors
- Not using correct time proportion for partial hours
- Forgetting to reference all tides to same HW time
- Plotting vectors in wrong sequence
- Mixing True and magnetic directions

## Assessment
- Integrate 3 tidal vectors and find resultant within ±5° and ±0.2 NM
- Handle 2 partial-hour segments correctly
- Apply resultant to plot EP on chart
- Demonstrate time savings vs hourly plotting