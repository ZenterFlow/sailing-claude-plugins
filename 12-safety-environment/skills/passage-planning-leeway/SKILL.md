---
name: "Passage Planning with Leeway Calculation"
version: "1.0.0"
triggers:
  - "passage planning"
  - "leeway calculation"
  - "eta calculation"
  - "shore contact"
  - "latest arrival"
  - "solas v"
---

# Passage Planning with Leeway Calculation

## Purpose
Develop comprehensive passage plans considering tidal effects, vessel leeway characteristics, and regulatory requirements while establishing reliable shore-based monitoring systems for offshore voyages.

## Description
This skill covers leeway assessment and calculation, ETA computation with safety margins, shore contact information packages, pre-departure verification, and regulatory compliance (SOLAS V Regulation 34).

## Activation Triggers
Use this skill when you need to:
- Calculate leeway allowances for vessel type and conditions
- Account for tidal stream effects in ETA computations
- Prepare detailed voyage information for shore contacts
- Apply appropriate safety margins for weather delays
- Comply with SOLAS V passage planning requirements

## Behaviour

### Leeway Assessment and Calculation

**Leeway Factors by Vessel Characteristics:**
- **Bilge Keel/High Windage Vessels:** Greater leeway
- **Deep Keel/Long Keel:** Reduced leeway due to better lateral resistance
- **Motor Cruisers:** Higher freeboard increases windage despite higher speeds
- **Light Winds:** Increase leeway due to reduced water flow over foils
- **Angle of Heel:** Greater heel increases underwater profile exposed to lateral forces

**Measuring Leeway Underway:**
1. **Take Wake Bearing:** Use hand bearing compass on vessel's wake
2. **Calculate Difference:** Compare wake bearing angle to reciprocal of course steered
3. **Record Data:** Document leeway angle for given conditions
4. **Build Reference Table:** Create matrix of leeway vs. wind direction, speed, heel

### Passage Planning Calculations

**ETA Computation with Leeway:**
1. **Calculate Base Time:** Distance ÷ Estimated Speed
2. **Add Leeway Component:** Light wind & slow speed: Add 10-20% time allowance; Strong wind & high windage: Add 20-30%
3. **Add Tide Effect:** Calculate tidal stream component along track
4. **Apply Safety Margin:** Add 15-30% buffer for unforeseen delays
5. **Determine "Latest Arrival":** Critical time to raise alarm with shore contact

### Shore Contact Information Package

**Required Voyage Details:**
- **Route Description:** Start/end points with intermediate ports
- **Timing:** ETA at each destination and OUTSIDE LATEST arrival time
- **Refuge Ports:** Proposed ports of refuge en route
- **Vessel Specifications:** Type, length, registration, crew count, provisions duration
- **Safety Equipment:** List of carried equipment (life raft, EPIRB, flares, etc.)
- **Communication:** VHF channels, DSC MMSI number, satellite phone if fitted

**Communication Methods:**
- **Coastguard Registration:** Use RYA Safetrx app or radio voyage plan
- **Club/Organization:** Submit movement form to marina or yacht club
- **Designated Contact:** Provide detailed instructions to shore-based person

### Pre-Departure Verification

- **Fuel:** Tanks filled to 7/8 maximum capacity
- **Water:** Minimum 2 liters per person per day plus cooking needs
- **Gas:** Full bottle with spare if passage > 7 days
- **Provisions:** Non-perishable food for voyage duration + 50% reserve
- **Clothing:** Warm waterproof gear for all crew
- **Bedding:** Dry, adequate for expected temperatures

### Regulatory Context

- **Written Passage Plan:** Legal requirement for proceeding to sea (SOLAS V Regulation 34)
- **Logbook Entries:** Record departure time and initial position
- **Evidence Preservation:** Logbook and passage plan become legal evidence if incident occurs
- **MAIB:** Marine Accident Investigation Branch conducts inquiries; failure to plan demonstrates negligence

## Common Errors to Avoid

- Failing to account for leeway in ETA calculations
- Providing shore contact with ETA but not "latest arrival" time
- Insufficient fuel reserve (less than 20% above calculated needs)
- Not documenting leeway measurements for future reference
- Omitting proposed ports of refuge from passage plan
- Underestimating leeway for vessels with high freeboard

## Assessment Criteria

Competency demonstrated by:
- Calculating leeway angle from wake bearing observation
- Computing ETA including leeway allowance and tidal stream effect
- Preparing complete shore contact information package
- Demonstrating reference table construction for leeway data logging
- Explaining legal implications of passage planning under SOLAS V
- Showing proper fuel filling technique to 7/8 capacity

---

**Version:** 1.0.0
**Last Updated:** 2025-11-10
**Part of:** Plugin 12 - Safety & Environment
