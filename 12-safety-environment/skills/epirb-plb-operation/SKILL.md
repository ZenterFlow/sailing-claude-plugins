---
name: "Emergency Position Indicating Devices Operation (EPIRB/PLB/AIS)"
version: "1.0.0"
triggers:
  - "epirb"
  - "plb"
  - "personal locator beacon"
  - "sart"
  - "personal ais"
  - "406 mhz"
---

# Emergency Position Indicating Devices Operation (EPIRB/PLB/AIS)

## Purpose
Activate, deploy, and distinguish between EPIRBs, PLBs, and personal AIS beacons for emergency position transmission, understanding coverage limitations and registration requirements for each device type.

## Description
This skill covers device activation and operation for EPIRBs, PLBs, personal AIS, and SARTs, transmission characteristics, device selection matrix, and registration requirements.

## Activation Triggers
Use this skill when you need to:
- Activate EPIRB and PLB correctly in emergency
- Differentiate device coverage ranges and receiving stations
- Understand registration requirements
- Select appropriate device for vessel vs personal use
- Understand SART radar homing procedures

## Behaviour

### EPIRB (Emergency Position Indicating Radio Beacon)

**Activation Method:**
1. **Manual Activation:** Remove from bracket, deploy antenna, switch to ON
2. **Automatic Activation:** Water sensor triggers when submerged (hull-mounted units)
3. **Activation Indication:** LED flashes and audible beep confirms transmission

**Transmission Characteristics:**
- **Frequency:** 406 MHz primary distress frequency
- **Signal Content:** Vessel identification, GPS coordinates, emergency nature
- **Satellite System:** COSPAS-SARSAT global coverage
- **Range:** Global (worldwide satellite reception)
- **Registration:** MUST be registered to vessel with coastguard - NOT transferable vessel-to-vessel without re-registration

**Mounting Requirements:**
- **Best Location:** Easy access in rough weather, typically near helm
- **Avoid Accidental Activation:** Not in location where it can be bumped
- **Float-Free:** Category I EPIRBs must be in automatic release bracket

### PLB (Personal Locator Beacon)

**Activation Method:**
1. **Deploy Antenna:** Pull antenna to full extension
2. **Power On:** Press and hold activation button (typically 3+ seconds)
3. **Position Acquisition:** Wait 2-5 minutes for GPS lock
4. **Confirmation:** LED sequence indicates successful transmission

**Transmission Characteristics:**
- **Frequency:** 406 MHz (same satellite system as EPIRB)
- **Range:** Global satellite reception
- **GPS Integration:** Internal GPS provides position coordinates
- **Subscription:** No subscription fees (one-time purchase)
- **Registration:** Registered to PERSON, not vessel - portable across vessels, land use

**Key Differences from EPIRB:**
- **Portability:** Can be carried ashore for hiking/mountaineering
- **Battery Life:** Typically 24 hours vs 48+ hours for EPIRB
- **Activation:** Manual only (no automatic water activation)
- **Buoyancy:** May not be buoyant (check model specifications)
- **Compliance:** NOT part of GMDSS - may not meet same standards as EPIRB

### Personal AIS (Automatic Identification System)

**Activation Method:**
- **Water Activation:** Contact with water automatically activates
- **Manual Activation:** Press button to activate SOS strobe and transmission

**Transmission Characteristics:**
- **System:** VHF-based AIS network
- **Range:** Typically 4 nautical miles (VHF line-of-sight)
- **Signal Content:** MOB alert with GPS coordinates transmitted to all AIS-equipped vessels
- **Visual Alert:** Powerful integral strobe light, often with SOS pattern
- **Subscription:** No fees (uses AIS infrastructure)

**Limitations:**
- **Range Restricted:** Requires receiving vessel/station within VHF range
- **Not Satellite:** Will not alert rescue services directly
- **AIS Requirement:** Only vessels with AIS receivers will detect alarm
- **Offshore Use:** Limited effectiveness beyond coastal waters

### SART (Search And Rescue Transponder)

**Activation Method:**
1. **Manual Switch:** Turn to ON position
2. **Automatic Standby:** Some models activate on water contact
3. **Radar Interrogation:** Responds to X-band radar signals (9 GHz)

**Radar Display Pattern:**
- **Visual Appearance:** Series of 12 dots or arcs on radar screen
- **Pattern:** Forms line pointing directly to SART location
- **Range:** Limited by radar power (typically 5-10 nautical miles)
- **Homing:** Allows rescue vessel to steer directly along dotted line to beacon

### Device Selection Matrix

**For Vessel Emergency (12+ m vessels):**
- **Primary:** EPIRB (registered to vessel)
- **Secondary:** SART (for radar homing by rescuers)
- **Backup:** PLB for skipper (if abandoning vessel)

**For Personal Safety (all crew):**
- **Offshore:** PLB (global coverage, satellite alert)
- **Coastal/Inshore:** Personal AIS (alerts nearby vessels rapidly)
- **Best Practice:** Carry both PLB and personal AIS when offshore

### Registration Requirements

- **EPIRB:** Vessel details (name, MMSI, description, emergency contacts)
- **PLB:** Personal details (name, address, emergency contacts, medical info)
- **Update Frequency:** Annually or when details change
- **False Alerts:** Contact rescue center immediately if accidental activation occurs

## Common Errors to Avoid

- Activating EPIRB when PLB would be more appropriate (and vice versa)
- Not registering device or failing to update registration
- Expecting personal AIS to work beyond VHF range offshore
- Storing EPIRB where it cannot be accessed in rough weather
- Failing to understand that PLB is not GMDSS-compliant
- Accidental SART activation by improper stowage location

## Assessment Criteria

Competency demonstrated by:
- Demonstrating correct EPIRB activation sequence including antenna deployment
- Explaining key differences between EPIRB and PLB
- Identifying optimal mounting location for SART and justifying choice
- Predicting radar display pattern when SART is interrogated
- Calculating expected range of personal AIS in 2m wave height conditions
- Showing PLB registration documentation and explaining update requirements
- Determining appropriate device selection for coastal day sail vs offshore passage

---

**Version:** 1.0.0
**Last Updated:** 2025-11-10
**Part of:** Plugin 12 - Safety & Environment
