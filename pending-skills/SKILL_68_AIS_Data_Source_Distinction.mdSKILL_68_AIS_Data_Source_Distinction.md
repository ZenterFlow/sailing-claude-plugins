# SKILL: AIS Data Source Distinction (Direct vs Internet)

## Description
Distinguish between direct VHF AIS data on chart plotter and internet-shared AIS data, understanding the advantages of direct AIS for collision avoidance.

## Prerequisites
- AIS interpretation (SKILL_56)

## Learning Objectives
- Identify AIS data source (direct VHF vs internet)
- Explain advantages of direct VHF AIS
- Understand limitations of internet AIS
- Recognize why chart plotter AIS is superior for navigation
- Distinguish real-time vs delayed AIS data

**AIS Data Sources:**
**Direct VHF AIS (Chart Plotter):**
- **Reception:** VHF antenna receives signals directly from vessels
- **Latency:** Real-time, &lt;1 second delay
- **Coverage:** 10-20 NM typical range (VHF line of sight)
- **Alarms:** Full CPA/TCPA alarms on plotter
- **Reliability:** Independent of internet/cell service
- **Update rate:** Every 2-10 seconds (vessel dependent)
- **Best for:** Collision avoidance, close-quarters navigation

**Internet AIS (Websites/Apps):**
- **Source:** Shore stations receive VHF and upload to internet
- **Latency:** 30 seconds to several minutes delay
- **Coverage:** Global (where shore stations exist)
- **Alarms:** Usually none or limited
- **Reliability:** Requires internet/cell connection
- **Update rate:** Depends on network, often delayed
- **Best for:** General monitoring, vessel tracking, planning

**Chart Plotter Repeater Apps:**
- **Direct AIS:** If connected to main plotter receiving VHF
- **Advantage:** Real-time data on mobile device
- **Alarms:** May be limited on mobile (depends on app)
- **Key benefit:** Mobility while maintaining direct data quality

**Practical Implications:**
**Collision Avoidance:**
- **Direct AIS:** Reliable for real-time decision making
- **Internet AIS:** Too delayed for close-quarters use
- **Example:** 12 knot vessel moves 100m in 15 seconds
- **Delay impact:** Internet delay could show false safe position

**Navigation Planning:**
- **Internet AIS:** Good for checking area traffic density
- **Direct AIS:** Essential for monitoring during passage

**Alarm Capability:**
- **Chart plotter:** Full CPA/TCPA audio/visual alarms
- **Mobile repeater:** Often lacks audio alarms
- **Internet app:** Typically no alarms

**Coverage Gaps:**
- **Direct AIS:** Limited by VHF range, but reliable within range
- **Internet AIS:** Gaps in remote areas without shore stations
- **Offshore:** Direct AIS may be only source

## Common Errors
- Using internet AIS for real-time collision avoidance
- Assuming all AIS sources are equally reliable
- Not understanding delay in internet AIS
- Expecting full alarms on mobile AIS apps

## Assessment
- Identify data source from system description
- Explain why direct AIS is better for collision avoidance
- Calculate vessel movement during typical delays
- Evaluate mobile repeater app vs internet AIS
- Determine appropriate AIS source for given scenario