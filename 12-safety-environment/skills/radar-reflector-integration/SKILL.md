---
name: "Radar Reflector Installation and AIS Integration"
version: "1.0.0"
triggers:
  - "radar reflector"
  - "ais integration"
  - "arpa marpa"
  - "radar cross section"
  - "reflector installation"
  - "target tracking"
---

# Radar Reflector Installation and AIS Integration

## Purpose
Install, maintain, and integrate radar reflectors and AIS systems to maximize vessel detection by other ships, understanding the complementary roles of both technologies in collision avoidance.

## Description
This skill covers radar reflector type selection and installation optimization, AIS system integration for collision avoidance, ARPA/MARPA capabilities, and the complementary use of both technologies for maximum vessel detection.

## Activation Triggers
Use this skill when you need to:
- Select appropriate reflector type based on vessel construction
- Install reflector for maximum radar cross-section effectiveness
- Interpret AIS data to supplement radar collision avoidance
- Understand ARPA/MARPA capabilities for target tracking
- Integrate multiple detection systems

## Behaviour

### Radar Reflector Installation

**Reflector Type Selection:**

**Fixed Octahedral Reflector:**
- **Construction:** Rigid plastic or metal plates forming multi-angle reflector
- **Advantages:** Always deployed, superior effectiveness, no deployment action required
- **Disadvantages:** Windage aloft, potential for damage in extreme conditions
- **Best For:** Vessels that regularly operate in shipping lanes or poor visibility

**Collapsible Reflector:**
- **Construction:** Folds flat, opens to octahedral shape with internal springs
- **Advantages:** Lower cost, removable, less windage when stowed
- **Disadvantages:** Manual deployment required, inferior performance to fixed
- **Best For:** Occasional use, budget-conscious, racing vessels where weight critical

**Active (Powered) Reflector:**
- **Construction:** Electronic device that amplifies and returns radar signal
- **Advantages:** Very strong return, adjustable output
- **Disadvantages:** Requires power, more expensive, potential for failure
- **Best For:** Large vessels, commercial applications
- **Limitation:** Not ideal for sailing vessels due to power consumption

### Installation Optimization

**Height Requirements:**
- **Minimum Height:** 4 meters above waterline (higher is better)
- **Practical Limit:** Just below masthead to avoid interfering with instruments
- **Motor Vessels:** Mount on radar arch, mast, or pole on cabin top
- **Sailing Vessels:** Mast-mounted, preferably in permanent position

**Positioning for Maximum RCS:**
- **Clear Line of Sight:** No rigging, antennas, or equipment blocking reflector faces
- **Free Rotation:** Allow reflector to rotate presenting all angles to scanning radar
- **Stability:** Secure mounting that doesn't swing excessively in seaway

### AIS Integration for Collision Avoidance

**AIS Display Information:**
- **Vessel Name:** Identity of target vessel
- **MMSI:** Unique identification number
- **Course and Speed:** Real-time navigation data
- **Closest Point of Approach (CPA):** Calculated minimum distance
- **Time to CPA (TCPA):** Time until closest approach
- **Vessel Type and Dimensions:** Size and category classification

**AIS Advantages Over Radar:**
- **Positive Identification:** Know vessel name and type immediately
- **Voice Contact:** Can call vessel directly on VHF using MMSI
- **Behind Obstacles:** AIS signals pass through land features where radar fails
- **Small Vessel Detection:** Better than radar for detecting small craft with AIS

**AIS Limitations:**
- **Not Universal:** Many small craft do not carry AIS
- **Data Quality:** Relies on other vessel's correct data entry
- **Overreliance Risk:** Must still maintain radar watch and visual lookout
- **Update Rate:** Typically slower update than radar (2-10 seconds vs real-time)

### ARPA/MARPA Capabilities

**Automatic Radar Plotting Aid (ARPA):**
- **Automatic Target Acquisition:** System automatically tracks all targets
- **CPA/TCPA Calculation:** Continuous computation for all targets
- **Collision Alarms:** Automatic warnings when CPA/TCPA thresholds breached
- **Trial Maneuver:** Test course/speed changes before executing
- **Target History:** Shows past track of target vessels

**Manual  Radar Plotting Aid (MARPA):**
- **Manual Target Selection:** Operator selects targets to track
- **Limited Tracking:** Typically tracks fewer targets than ARPA
- **Similar Functions:** CPA/TCPA calculation, collision warnings
- **Lower Cost:** More affordable than full ARPA system

### Integrated System Use

**Complementary Detection Strategy:**
1. **Radar:** Primary detection, especially in poor visibility
2. **AIS:** Identification and communication
3. **Visual:** Confirmation and backup
4. **Radar Reflector:** Ensure own vessel is detected by others

**Collision Avoidance Workflow:**
1. **Detect:** Radar or AIS identifies potential target
2. **Identify:** AIS provides vessel details
3. **Assess:** ARPA/MARPA calculates CPA/TCPA
4. **Verify:** Visual confirmation when in range
5. **Communicate:** VHF contact if intentions unclear
6. **Act:** Execute collision avoidance maneuver if required

## Common Errors to Avoid

- Installing reflector too low on mast for effective RCS
- Relying solely on AIS without radar backup
- Assuming all vessels carry AIS transponders
- Not maintaining radar reflector (corrosion, damage)
- Blocking reflector with rigging or equipment
- Expecting collapsible reflector to work without deployment
- Over-trusting ARPA data without visual verification

## Assessment Criteria

Competency demonstrated by:
- Selecting appropriate reflector type based on vessel characteristics
- Calculating optimal mounting height for radar reflector
- Interpreting AIS target data and determining collision risk
- Explaining ARPA trial maneuver function and use case
- Demonstrating integrated use of radar, AIS, and visual lookout
- Identifying scenarios where AIS fails but radar succeeds
- Troubleshooting poor radar reflector performance

---

**Version:** 1.0.0
**Last Updated:** 2025-11-10
**Part of:** Plugin 12 - Safety & Environment
