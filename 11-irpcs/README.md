# Plugin 11: IRPCS (International Regulations for Preventing Collisions at Sea)

**Status**: ✅ Complete - Production Ready (v1.3.0)

Master the International Regulations for Preventing Collisions at Sea (IRPCS/ColRegs) with comprehensive coverage of collision avoidance rules, vessel hierarchy, lights and shapes, sound signals, and practical decision-making.

## Overview

This plugin provides complete IRPCS/ColRegs instruction covering all 38 rules, from basic watchkeeping to complex multi-vessel encounters. Essential for RYA/ASA YachtMaster certification and safe navigation in all conditions.

## Skills Included (7)

### 1. Fundamentals & Watchkeeping
**general-rules-watchkeeping** - Master fundamental watchkeeping requirements, blind arc identification, risk of collision assessment, and stand-on/give-way actions under Rules 5-9.

**Topics:**
- Rule 5 (Lookout) by all available means
- Blind arc identification and mitigation
- Risk assessment methods (constant bearing)
- Stand-on vs give-way vessel actions
- Narrow channel rules (Rule 9)
- Regulatory language ("shall" vs "may")

### 2. Traffic Management
**traffic-separation-impeding** - Navigate Traffic Separation Schemes correctly, understand impeding obligations, and apply vessel hierarchy rules under Rules 10 and 18.

**Topics:**
- TSS lane usage, joining, leaving, crossing procedures
- Inshore traffic zone eligibility
- Separation zone restrictions
- Vessel hierarchy (NUC > RAM > CBD > Fishing > Sail > Power)
- "Impede" vs "give way" critical distinction
- Special vessel identification (CBD, RAM, NUC)

### 3. Visual Identification (Day)
**day-shapes-identification** - Identify vessel types and operational status from day shapes, interpret combined light/shape displays under Rules 20-31.

**Topics:**
- All standard day shapes (ball, cone, diamond, cylinder)
- Vessel at anchor/aground shapes
- NUC, RAM, fishing, towing shapes
- Underwater operations obstruction markings
- Motor sailing cone (apex down)
- Combined light/shape interpretation

### 4. Visual Identification (Night)
**navigation-lights-sound-signals** - Interpret navigation light configurations, calculate light arc coverage, and execute correct sound signals under Rules 20-37.

**Topics:**
- Basic light arcs (port 112.5°, starboard 112.5°, stern 135°, steaming 225°)
- Vessel length and light visibility ranges
- Sailing vessel options (tricolour vs separate lights)
- Motor sailing requirements (tricolour OFF)
- Special vessel configurations (NUC, RAM, CBD, fishing)
- Fog signals for all vessel types
- Maneuvering and warning signals

**light-arcs-vessel-length** - Calculate navigation light coverage arcs, determine vessel length from light configurations, and identify aspect angles.

**Topics:**
- Light arc calculations and total coverage
- Vessel length from light visibility ranges
- One vs two masthead lights (50m threshold)
- Tricolour restrictions (<20m, sailing only)
- Identifying vessel aspect from visible lights
- Underway vs making way distinctions
- Motor sailing light configuration requirements

### 5. Collision Avoidance Actions
**collision-avoidance-decisions** - Execute correct collision avoidance actions based on vessel hierarchy, encounter type, and visibility conditions under Rules 13-19.

**Topics:**
- Turn-to-starboard principle
- Head-on situation (Rule 14) - both turn to starboard
- Crossing situation (Rule 15) - starboard gives way
- Overtaking situation (Rule 13) - overtaking vessel gives way
- Stand-on vessel responsibilities (Rule 17)
- Multiple vessel encounters
- Restricted visibility rules (Rule 19)
- Danger signal (5+ short blasts)
- Last-minute avoiding action

**risk-assessment-stand-on-actions** - Master systematic risk of collision assessment methods and proper stand-on vessel responsibilities under Rules 6, 7, and 17.

**Topics:**
- Visual bearing series (constant bearing = risk)
- Radar observation (CPA/TCPA calculations)
- Auditory detection (fog signal identification)
- AIS monitoring and limitations
- Stand-on vessel primary obligations
- When last-resort action is required
- Safe speed determination factors (Rule 6)
- "If in doubt" principle (Rule 7)
- Emergency actions and documentation

## Teaching Approach

### Progressive Learning Path
1. **Foundation:** Watchkeeping, risk assessment, basic definitions
2. **Identification:** Lights, shapes, sound signals
3. **Hierarchy:** Vessel types and pecking order
4. **Situations:** Head-on, crossing, overtaking
5. **Complex:** TSS, multiple vessels, restricted visibility
6. **Integration:** Complete collision avoidance decision-making

### Key Principles Emphasized
- **No Right of Way:** IRPCS never grants "right of way" - all vessels must avoid collision
- **"Shall" = Mandatory:** Non-negotiable legal requirements
- **Early and Substantial Action:** Small, late alterations are dangerous
- **Turn to Starboard:** Preferred action unless other rules apply
- **If in Doubt, Assume Risk:** Precautionary principle always applies

## Critical Rules Summary

### Vessel Hierarchy (Rule 18)
From highest to lowest priority:
1. Not Under Command (NUC) - 2 red lights/balls
2. Restricted in Ability to Manoeuvre (RAM) - red-white-red/ball-diamond-ball
3. Constrained by Draught (CBD) - 3 red lights/cylinder *(special case: impede but not give-way)*
4. Fishing - red/white or green/white lights, double cone
5. Sailing - under sail alone
6. Power - including motor-sailing

### Common Encounter Types

**Head-On (Rule 14):**
- See both sidelights (red and green)
- Both vessels turn to starboard
- Pass port-to-port

**Crossing (Rule 15):**
- Vessel with other on starboard = give-way
- Vessel with other on port = stand-on
- Give-way vessel preferably turns to starboard

**Overtaking (Rule 13):**
- More than 22.5° abaft beam = overtaking
- Overtaking vessel always give-way
- Continues until finally past and clear

### Sound Signals Quick Reference

**In Sight (Maneuvering):**
- 1 short = altering to starboard
- 2 short = altering to port
- 3 short = engines astern
- 5+ short = danger signal

**Restricted Visibility (Fog):**
- 1 long = power vessel making way
- 2 long = power vessel stopped
- 1 long + 2 short = sail, RAM, NUC, fishing, towing
- 1 long + 3 short = last vessel in tow
- 4 short = pilot vessel

## Usage Examples

### Example 1: Identify Vessel from Lights at Night
```
User: "I see a green light and a white masthead light. What vessel type and what should I do?"

IRPCS Tutor (using light-arcs-vessel-length):
"You're seeing a power vessel's starboard side (green sidelight + masthead steaming light).

**Situation Analysis:**
- Vessel Aspect: You see the starboard side = you are on their port side
- If Crossing: You are the give-way vessel (vessel on your starboard has right to stand-on)
- Action Required: Alter course to starboard (turn away), keeping well clear

**Risk Assessment:**
- Take compass bearings at 1-2 minute intervals
- If bearing remains constant while distance decreases = high collision risk
- Take early and substantial action to show clear intent

**Give-Way Action:**
- Alter to starboard significantly (preferred)
- Show the other vessel a different aspect
- Maintain new course until well clear"
```

### Example 2: TSS Navigation
```
User: "I'm in a 15m sailing yacht approaching a TSS. What are my obligations?"

IRPCS Tutor (using traffic-separation-impeding):
"As a sailing vessel <20m, you have specific TSS obligations:

**Inshore Zone Usage (Rule 10d):**
✓ You MAY use the inshore traffic zone (sailing vessels are permitted)
✓ Consider using it if safe rather than crossing lanes

**If Crossing the TSS:**
- Cross at RIGHT ANGLES to traffic flow (Rule 10c)
- Makes your intention clear to lane traffic
- Maintain steady speed and heading during crossing
- Avoid stopping in the lane

**If Using a Traffic Lane:**
- Proceed in general direction of traffic flow
- Keep to starboard side of lane
- Join/leave at lane termination points if possible
- Or join/leave at smallest angle to traffic flow

**Hierarchy Awareness:**
- You must not impede power vessels using the lane
- But if collision risk develops, normal crossing rules apply
- Still maintain proper lookout by all available means"
```

### Example 3: Stand-On Vessel Last Resort
```
User: "I'm the stand-on vessel in a crossing situation, but the give-way vessel isn't taking action. What should I do?"

IRPCS Tutor (using risk-assessment-stand-on-actions):
"Rule 17(b) - Stand-On Vessel Last Resort Action:

**Initial Obligation (Rule 17a):**
✓ You correctly maintained course and speed
✓ Monitored the give-way vessel

**When to Take Action:**
When it becomes apparent the give-way vessel is NOT taking appropriate action:
- Collision cannot be avoided by give-way vessel action alone
- Distance closing to unsafe range
- Constant bearing with decreasing distance

**Required Action:**
1. **Turn Away:** Alter course AWAY from the other vessel
2. **Starboard Preferred:** Turn to starboard if possible (shows clear intent)
3. **Substantial Alteration:** Large, obvious course change
4. **May Stop:** Reduce speed or stop engines if necessary
5. **Sound Signal:** 5+ short blasts (danger signal) to alert other vessel

**Prohibited Actions:**
✗ Do NOT turn to port for vessel on your port side
✗ Do NOT make small, hesitant alterations
✗ Do NOT delay action hoping give-way vessel will act

**Critical Timing:**
- Act early enough for action to be effective
- Don't wait until last second
- Deliberate, controlled maneuver (not panic reaction)"
```

## Target Audience

- RYA/ASA YachtMaster candidates
- Commercial vessel crew studying for certifications
- Recreational sailors in congested waters
- Anyone navigating in international waters
- Collision regulations exam preparation

## Prerequisites

- Basic vessel handling and terminology
- Understanding of compass bearings
- Familiarity with nautical charts

## Integration with Other Plugins

- **Plugin 08 (Visual Aids):** Navigation marks and lights complement IRPCS lights
- **Plugin 09 (Pilotage):** Pilotage procedures apply IRPCS in restricted waters
- **Plugin 05 (Electronic Navigation):** Radar and AIS support IRPCS risk assessment
- **Plugin 10 (Meteorology):** Weather impacts visibility and safe speed decisions

## Exam Preparation Notes

IRPCS is heavily tested on RYA YachtMaster and USCG license exams:
- Rule numbers and specific wording are important
- Scenario-based questions are common
- Light and shape identification is critical
- Sound signal sequences must be memorized
- Vessel hierarchy must be automatic

## Version History

- **v1.3.0** (2025-11-10): Complete implementation - 7 comprehensive IRPCS skills covering all collision regulations
- **v0.1.0** (2025-10-31): Skeleton plugin created

## License

Part of the Sailing Claude Plugins educational resource.
