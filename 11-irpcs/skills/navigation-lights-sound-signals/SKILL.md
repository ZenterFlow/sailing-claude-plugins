---
name: "Navigation Lights and Sound Signals"
version: "1.0.0"
triggers:
  - "navigation lights"
  - "sidelights"
  - "tricolour"
  - "motor sailing lights"
  - "fog signals"
  - "sound signals"
  - "maneuvering signals"
---

# Navigation Lights and Sound Signals

## Purpose
Interpret navigation light configurations, calculate light arc coverage, and execute correct sound signals for various vessel operations and visibility conditions under IRPCS Rules 20-37.

## Description
This skill covers all navigation light configurations (Rules 20-31) and sound signal requirements (Rules 32-37). Essential for identifying vessels at night, determining vessel type and status, and communicating intentions through proper signaling.

## Activation Triggers
Use this skill when you need to:
- Identify vessel type from light display
- Calculate light arc angles
- Understand tricolour vs separate light configurations
- Learn motor sailing light requirements
- Execute fog signals correctly
- Apply maneuvering and warning sound signals

## Behaviour

### Navigation Light Fundamentals

**Basic Light Arcs:**
- **Port Sidelight:** Red, 112.5° arc (22.5° abaft the beam to dead ahead)
- **Starboard Sidelight:** Green, 112.5° arc (22.5° abaft the beam to dead ahead)
- **Stern Light:** White, 135° arc (67.5° each side of dead astern)
- **Steaming Light (Masthead):** White, 225° arc (forward-facing)
- **Total Coverage:** 360° when all lights displayed

### Vessel Length and Light Visibility Ranges

**Motor Vessels <7m, Speed <7 knots:**
- **Minimum:** All-round white light (optional sidelights)
- **Visibility:** White 2nm, sidelights (if carried) 1nm

**Motor Vessels 7m - 12m:**
- **Standard:** Masthead light (2nm), stern light (2nm), combined bicolour sidelights (1nm)
- **Alternative:** Sidelights + all-round white light (instead of masthead/stern)
- **Masthead Height:** At least 2.5m above sidelights

**Motor Vessels 12m - 50m:**
- **Masthead Light:** 5nm visibility (3nm if <20m length)
- **Stern Light:** 2nm visibility
- **Sidelights:** 2nm visibility

**Motor Vessels >50m:**
- **Additional Light:** Forward white light (arc 225°) lower and forward of main masthead
- **Visibility:** Masthead 6nm, sidelights/stern 3nm

### Sailing Vessel Lights (<20m) - Two Display Options

**Option 1 - Separate Lights:**
- **Port/Starboard Lights:** At bow, 112.5° each
- **Stern Light:** 135° white at stern
- **Alternative Addition:** Red over green all-round lights at masthead (optional)

**Option 2 - Tricolour (Masthead):**
- **Combined:** Red, green, white in single fixture at masthead
- **Restriction:** Use ONLY when sailing, NOT when motoring
- **Arcs:** Same as separate lights but combined

**Critical Rule:** NEVER display tricolour with bicolour, stern, or steaming lights

### Motor Sailing Lights (Rule 25)

**Requirements:**
- **Day Shape:** Cone pointing down (apex downward)
- **Night Lights:** Steaming light + sidelights + stern light
- **Tricolour:** Must be OFF when motor sailing
- **Fog Signal:** 1 long blast every 2 minutes (power vessel signal)

**Why Tricolour Prohibited:**
Prevents confusion - showing both sailing and power status simultaneously violates IRPCS

### Special Vessel Light Configurations

**Not Under Command (NUC):**
- **Lights:** Two vertical red all-round lights
- **Making Way:** Add sidelights and stern light
- **Fog Signal:** 1 long + 2 short blasts

**Restricted in Ability to Manoeuvre (RAM):**
- **Lights:** Red-white-red vertical all-round lights
- **Making Way:** Add masthead, sidelights, stern light
- **Fog Signal:** 1 long + 2 short blasts

**Constrained by Draught (CBD):**
- **Lights:** Three vertical red lights
- **Day Shape:** Cylinder
- **Fog Signal:** 1 long + 2 short blasts

**Fishing Vessels - Trawling:**
- **Lights:** Green over white vertical, plus masthead light abaft
- **Shape:** Two cones apexes together
- **Fog Signal:** 1 long + 2 short blasts

**Fishing Vessels - Other Fishing:**
- **Lights:** Red over white vertical
- **Shape:** Two cones apexes together
- **Gear Warning:** All-round white light if gear extends >150m

**Vessel Engaged in Underwater Operations:**
- **Lights:** Red-white-red vertical plus red/green obstruction lights
- **Shapes:** Ball-diamond-ball plus obstruction marks
- **Clear Side:** Green lights/two diamonds indicate safe passing side

### Vessels at Anchor

**<50m Length:**
- **Light:** One all-round white light where best seen

**>50m Length:**
- **Forward Light:** All-round white in forepart
- **Aft Light:** Additional all-round white lower and aft

**>100m Length:**
- **Deck Lights:** Available lights to illuminate decks

**Fog Signals for Anchored Vessels:**
- **<100m:** Rapid bell ringing (5 seconds) at intervals ≤1 minute
- **>100m:** Bell forward (5s) + gong aft (5s) + optional danger signal (short-long-short)

### Vessel Aground

- **Lights:** Anchor lights plus two vertical red lights
- **Shapes:** Three black balls vertical
- **Fog Signal:** Bell 3 strokes + rapid ringing + 3 strokes (≤1 minute intervals)

### Sound Signal Fundamentals

**Maneuvering Signals (In Sight):**
- **1 Short Blast:** Altering course to starboard
- **2 Short Blasts:** Altering course to port
- **3 Short Blasts:** Operating engines astern

**Warning Signals:**
- **5 Short Blasts:** "I do not understand your intentions" / Danger signal

**Fog Signals (Restricted Visibility):**

**Power Vessel Underway:**
- **Making Way:** 1 long blast every 2 minutes
- **Stopped:** 2 long blasts every 2 minutes

**Sailing Vessel Underway:** 1 long + 2 short blasts every 2 minutes

**Vessel Restricted in Ability to Manoeuvre:** 1 long + 2 short blasts every 2 minutes

**Vessel Constrained by Draught:** 1 long + 2 short blasts every 2 minutes

**Fishing Vessel:** 1 long + 2 short blasts every 2 minutes

**Vessel Towed (Last Vessel):** 1 long + 3 short blasts every 2 minutes

**Pilot Vessel on Duty:** 4 short blasts every 2 minutes

**Vessel at Anchor:** Rapid bell ringing (5s) at intervals ≤1 minute

**Vessel Aground:** 3 bell strokes + rapid ringing + 3 strokes (≤1 minute intervals)

**Diver Down Warning:** 1 short + 1 long blast every 2 minutes (Morse A)

**Agreement Signal:** 1 Long + 1 Short + 1 Long + 1 Short ("I agree with your intentions")

## Common Errors to Avoid

- Displaying tricolour when motor sailing (illegal and confusing)
- Forgetting steaming light when under power
- Using wrong fog signal for vessel type
- Not displaying anchor light when anchored
- Misidentifying vessel length from light configuration
- Confusing 2 short vs 3 short blast signals
- Using 5 short blasts as routine communication

## Assessment Criteria

Competency demonstrated by:
- Identifying vessel type and length from light display
- Calculating total arc coverage for given light configuration
- Selecting correct fog signal for vessel situation
- Determining if vessel is underway or making way from lights
- Designing proper light display for motor sailing scenario
- Interpreting sound signal sequence and responding appropriately
- Distinguishing special vessel types from light configurations

---

**Version:** 1.0.0
**Last Updated:** 2025-11-10
**Part of:** Plugin 11 - IRPCS (International Regulations for Preventing Collisions at Sea)
