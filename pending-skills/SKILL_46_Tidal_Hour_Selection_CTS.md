# SKILL: Tidal Hour Selection for Course to Steer

## Description
Determine the correct tidal hour offset (e.g., HW+2, HW-1) to use for CTS calculations based on departure time and trip duration.

## Prerequisites
- SKILL_27 (Tide Table Interpretation)
- SKILL_30 (Time Zones)
- SKILL_31 (Tidal Stream Usage)

## Learning Objectives
- Convert departure time to reference port time (Victoria)
- Calculate trip duration from ground track distance
- Select initial tidal hour for departure time
- Handle multi-hour trips with changing tides
- Apply time zone and DST conversions correctly

## Hour Selection Method
**Step 1: Identify Reference Port**
- Check tidal diamond table or atlas header
- RYA materials: typically HW Victoria
- Verify at top of table: "Tidal Stream Atlas: HW Victoria"

**Step 2: Convert Local Time to Reference Port Time**
- Start time given in local zone (e.g., SP DST, Zone -1)
- Convert to UT: apply DST and zone corrections
- May need to convert to Victoria zone if different

**Step 3: Determine HW at Reference Port**
- Look up HW time for date in tide tables
- Adjust for DST if needed
- This is your baseline (HW = 0 hours offset)

**Step 4: Calculate Trip Duration**
- Estimate from ground track distance ÷ boat speed
- Round to nearest 0.5 hour (30 min)
- CTS typically calculated for 1 hour vectors

**Step 5: Select Tidal Hour(s)**
- Hour 1: Identify departure time relative to HW
- Example: HW 1200, departure 1240 → HW+1 (1230-1330)
- Multi-hour trips: Use hourly tidal data for each hour
- Cross-hour trips: Pro-rate tide for partial hours

**Example:**
- Departure: 1240 UT
- HW Victoria: 1000 UT
- Time difference: +2 hours 40 minutes
- Falls in HW+2 hour (1200-1300)
- Use HW+2 tidal data for CTS calculation

## Multi-Hour Trip Considerations
- Trip &gt; 1 hour: Tidal set/drift changes each hour
- Options:
  1. Calculate CTS for first hour only, then re-evaluate
  2. Use average tide over trip duration
  3. Plot multiple tidal vectors (SKILL_33 method)
- For CTS, typically use first hour's tide only

## Common Errors
- Using local port HW instead of reference port
- Forgetting DST conversion
- Not rounding trip duration appropriately
- Using wrong hour offset (off by one hour)

## Assessment
- Correctly select tidal hour for 6 scenarios with different times/zones
- Explain hour selection logic for departure 15 min before HW
- Handle multi-hour trip tidal data selection
- Convert local time to Victoria HW reference correctly