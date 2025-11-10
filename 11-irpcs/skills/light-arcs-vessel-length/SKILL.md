---
name: "Navigation Light Arcs and Vessel Length Identification"
version: "1.0.0"
triggers:
  - "light arcs"
  - "vessel length identification"
  - "sidelight arcs"
  - "112.5 degrees"
  - "masthead lights"
  - "vessel aspect"
  - "underway making way"
---

# Navigation Light Arcs and Vessel Length Identification

## Purpose
Calculate navigation light coverage arcs, determine vessel length from light configurations, and identify aspect angles for collision avoidance under IRPCS Rules 20-31.

## Description
This skill covers detailed light arc calculations, vessel length determination from light visibility ranges and configurations, aspect angle identification from visible lights, and underway vs making way distinctions. Essential for accurate vessel identification and collision avoidance decision-making.

## Activation Triggers
Use this skill when you need to:
- Calculate total light coverage for various configurations
- Determine vessel length category from lights displayed
- Identify vessel aspect from visible lights
- Distinguish underway vs making way status
- Apply motor sailing light rules correctly
- Verify proper light configuration compliance

## Behaviour

### Light Arc Fundamentals

**Standard Arc Measurements:**
- **Port Sidelight:** 112.5° arc (covers 22.5° abaft beam to dead ahead)
- **Starboard Sidelight:** 112.5° arc (covers 22.5° abaft beam to dead ahead)
- **Combined Sidelights:** 225° total arc (112.5° + 112.5°)
- **Stern Light:** 135° arc (67.5° each side of dead astern)
- **Steaming Light (Masthead):** 225° arc (forward-facing)
- **Total 360° Coverage:** Sidelights (225°) + Stern Light (135°) = 360°

### Tricolour Light Arc (Sailing Vessel <20m)

**Combined Port/Starboard:**
- **Total Angle:** 225° arc
- **Coverage:** Combined red/green sectors of tricolour fixture
- **Restriction:** Use ONLY when sailing, NOT under power

**Stern Light (in tricolour):**
- **Angle:** 135° arc
- **Color:** White sector in tricolour fixture

**Total Tricolour Coverage:** 225° + 135° = 360°

### Power Vessel Light Arcs

**Bicolour Light:**
- **Port Section:** 112.5° red
- **Starboard Section:** 112.5° green
- **Total Bicolour:** 225° arc

**Stern Light:**
- **Angle:** 135° arc
- **Color:** White

**Steaming Light (Masthead):**
- **Angle:** 225° arc
- **Position:** Forward-facing, mounted on mast
- **Color:** White

**Total Coverage Check:**
- **Forward Coverage:** Bicolour (225°) + Steaming (225°) = Overlap forward
- **Aft Coverage:** Stern light (135°) fills astern sector
- **Complete:** 360° coverage achieved

### Motor Sailing Light Configuration

**Legal Requirement:**
- **Day:** Cone apex downward (visible shape)
- **Night:** Steaming light + sidelights + stern light
- **Prohibition:** Tricolour must be OFF

**Why Tricolour Prohibited:**
- **Confusion:** Shows both sailing and power status simultaneously
- **Misidentification:** Could be mistaken for separate sailing vessel
- **Rule Violation:** Clear IRPCS prohibition (Rule 25)

### Vessel Length Identification from Lights

**Power Vessels:**

**One Masthead Light Only:**
- **Length:** Probably under 50 meters
- **Categories:** Could be 12-50m
- **Visibility:** 5nm (20-50m) or 3nm (<20m)

**Two Masthead Lights (Forward and Main):**
- **Length:** Probably over 50 meters
- **Configuration:** Forward light lower and forward of main masthead
- **Visibility:** Main 6nm, forward same arc (225°), sidelights/stern 3nm

**Sidelight Visibility Ranges:**

**1 Nautical Mile:**
- **Vessel Size:** Typically under 12 meters
- **Configuration:** May be combined bicolour

**2 Nautical Miles:**
- **Vessel Size:** 12-20 meters
- **Configuration:** Separate sidelights or bicolour

**3 Nautical Miles:**
- **Vessel Size:** 20-50 meters or over 50 meters
- **Configuration:** Separate sidelights, matching stern visibility

### Sailing Vessel Length Indicators

**Tricolour Displayed:**
- **Maximum Length:** Under 20 meters (Rule 25 limitation)
- **Status:** Sailing only (not under power)

**Red Over Green Lights:**
- **Maximum Length:** Under 20 meters (optional additional lights)
- **Use:** With sidelights (not tricolour)

### Combined Light Displays

**Motor Sailing at Night:**
- **Lights Showing:** Steaming + sidelights + stern
- **Lights NOT Showing:** Tricolour (must be OFF)
- **Day Shape:** Cone apex down

**Sailing Only:**
- **Option 1:** Tricolour at masthead (under 20m)
- **Option 2:** Sidelights + stern light (any size)
- **Option 3 (if <20m):** Sidelights + stern + red/green masthead lights

### Identifying Vessel Aspect from Lights

**Seeing Both Sidelights (Red and Green):**
- **Aspect:** Head-on (bow approaching)
- **Your Action:** Both vessels alter to starboard, pass port-to-port
- **Rule:** Rule 14 (Head-on situation)

**Seeing Only Red Light (plus possibly masthead):**
- **Aspect:** Vessel's port side visible
- **Your Position:** To starboard of other vessel
- **Action:** If crossing, you are likely stand-on vessel

**Seeing Only Green Light (plus possibly masthead):**
- **Aspect:** Vessel's starboard side visible
- **Your Position:** To port of other vessel
- **Action:** If crossing, you are give-way vessel

**Seeing Only White Stern Light:**
- **Aspect:** Stern view (vessel going away)
- **Situation:** Overtaking (you are overtaking vessel)
- **Action:** You are give-way vessel, must keep clear

**Seeing Steaming Light + Sidelight:**
- **Aspect:** Forward quarter
- **Light Combination:** Determines exact aspect angle
- **Analysis:** Assess whether head-on or crossing

### Underway vs Making Way Light Differences

**Vessels Showing Making Way by Lights Alone:**
Only four types show making way status:
1. **RAM:** Aspect lights + type lights = making way
2. **NUC:** Aspect lights + type lights = making way
3. **Fishing (other):** Aspect lights + red/white type lights = making way
4. **Trawling:** Aspect lights + green/white type lights = making way

**All Other Vessels:**
- **Underway:** Type lights only (no aspect lights)
- **Making Way:** No light distinction (must infer from other indicators)
- **Example:** Power vessel shows same lights whether making way or drifting

### Detailed Length Categories

**Motor Vessel <7m, <7 knots:**
- **Option 1:** All-round white light only
- **Option 2:** All-round white + sidelights
- **Visibility:** White 2nm, sidelights 1nm (if carried)

**Motor Vessel 7-12m:**
- **Standard:** Masthead (2nm), stern (2nm), combined sidelights (1nm)
- **Alternative:** Sidelights + all-round white (instead of masthead/stern)
- **Masthead Height:** At least 2.5m above sidelights

**Motor Vessel 12-20m:**
- **Masthead:** 3 nautical miles visibility
- **Stern:** 2 nautical miles visibility
- **Sidelights:** 2 nautical miles visibility

**Motor Vessel 20-50m:**
- **Masthead:** 5 nautical miles visibility
- **Stern:** 2 nautical miles visibility
- **Sidelights:** 2 nautical miles visibility

**Motor Vessel >50m:**
- **Additional Light:** Forward white light (225°), lower and forward
- **Visibility:** Main masthead 6nm, sidelights/stern 3nm
- **Identification:** Distinctive two-masthead light configuration

### Practical Calculation Example

**Question:** Power vessel <20m with bicolour, steaming, stern lights - total arc coverage?

**Calculation:**
- Bicolour: 225° (port 112.5° + starboard 112.5°)
- Steaming: 225° (forward-facing)
- Stern: 135° (aft-facing)

**Forward Coverage:** Bicolour and steaming overlap significantly (both 225° forward)
**Aft Coverage:** Stern light 135° astern
**Total 360°:** Achieved through combination

**Verification:** 225° (forward sector) + 135° (astern sector) = 360° total coverage

## Common Errors to Avoid

- Calculating arcs incorrectly (forgetting sidelights are separate 112.5° each)
- Assuming tricolour can be used when motor sailing
- Misidentifying vessel length from insufficient light information
- Confusing underway vs making way light displays
- Forgetting two masthead lights indicate vessel over 50m
- Not recognizing that most vessels don't show making way status by lights

## Assessment Criteria

Competency demonstrated by:
- Calculating total light arc coverage for given vessel configuration
- Determining vessel length category from displayed lights
- Identifying aspect angle from visible light combination
- Distinguishing underway vs making way status from lights
- Designing proper light display for motor sailing vessel under 20m
- Troubleshooting incorrect light configuration scenarios
- Applying visibility ranges to determine vessel size

---

**Version:** 1.0.0
**Last Updated:** 2025-11-10
**Part of:** Plugin 11 - IRPCS (International Regulations for Preventing Collisions at Sea)
