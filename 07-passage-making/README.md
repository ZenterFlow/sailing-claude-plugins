# Plugin 07: Passage Making

**Status**: ✅ Complete - Comprehensive passage planning and preparation

**Purpose**: Complete passage planning workflow from pre-departure preparation through execution, covering safety briefings, equipment verification, passage calculations, and shore contact establishment. Essential for RYA/ASA YachtMaster Offshore certification.

---

## 🎯 Skills (5)

### 1. **almanac-navigator**
Extract harbor-specific information from nautical almanacs including VHF channels, high water differences, lock times, and pilotage notes.

**Coverage**:
- Port information and facilities
- VHF radio channels (marina, port authority, working channels)
- High water time differences
- Lock operating times and procedures
- Pilotage directions and entry notes
- Harbor regulations and berthing

**Key Use Cases**:
- Night harbor entry planning
- Lock timing calculations
- VHF channel selection
- Pilotage notes extraction

### 2. **pre-departure-safety-briefing**
Comprehensive safety briefing delivery and systematic equipment verification for all vessel types before departure.

**Coverage**:
- Life jacket inspection (bladder, gas bottle, crotch strap critical)
- Flare inventory verification (seal integrity, expiration dates)
- Fire extinguisher checks (AFFF for fuel, dry powder for electrical)
- Gas system inspection (external-draining locker, approved hoses)
- Safety equipment location briefing
- Emergency procedures (MOB, fire, flooding, Mayday)
- Crew responsibility assignment
- Shore contact establishment

**Critical Safety Points**:
- Crotch strap on life jackets prevents ride-up (critical)
- Flare seal integrity indicates usability
- Fire extinguisher service dates and types
- Gas shut-off valve locations (galley and main)

### 3. **lpg-gas-safety**
LPG system safety management, leak detection procedures, emergency ventilation, and fire prevention protocols.

**Coverage**:
- LPG storage requirements (external-draining locker)
- Approved hose specifications and replacement intervals
- Gas shut-off valve operation (galley and main bottle)
- Leak detection methods (soapy water, gas detectors)
- Emergency ventilation procedures
- Fire prevention during gas operations

**Critical Protocols**:
- NO electrical switches during gas leak (sparking risk)
- Ventilate thoroughly before investigating leak
- External-draining locker prevents gas accumulation in bilge
- Replace gas hoses every 5 years regardless of condition

### 4. **fire-safety-management**
Fire prevention strategies, extinguisher deployment procedures, and engine/galley/cabin fire protocols.

**Coverage**:
- Fire prevention and housekeeping
- Extinguisher types and selection (AFFF, dry powder, CO2)
- Engine compartment fire protocol (NEVER open bay)
- Galley fire response (turn off gas, smother flames)
- Cabin fire procedures (close hatches, ventilators)
- Extinguisher maintenance and service intervals

**Critical Engine Fire Protocol**:
1. NEVER open engine bay during fire (oxygen causes flashback)
2. Shut down engine immediately
3. Activate automatic fire suppression if fitted
4. Discharge extinguisher through access hole
5. Monitor temperature before opening

### 5. **passage-planning-leeway**
Comprehensive passage planning with leeway calculation, tidal effects, shore contact establishment, and SOLAS V compliance.

**Coverage**:
- Leeway assessment by vessel type and conditions
- Measuring leeway underway (wake bearing method)
- Building leeway reference tables
- ETA computation with leeway and tidal effects
- Shore contact information package
- "Latest arrival" time determination (critical)
- Pre-departure verification (fuel, water, gas, provisions)
- SOLAS V Regulation 34 compliance

**Leeway Calculation**:
- Take wake bearing with hand bearing compass
- Compare to reciprocal of course steered
- Document for given wind/heel conditions
- Build reference matrix for future planning

**Shore Contact Requirements**:
- Route description with refuge ports
- ETA AND "latest arrival" time (alarm trigger)
- Vessel specifications and crew count
- Safety equipment inventory
- Communication details (VHF, DSC MMSI, sat phone)

---

## 📖 Topics Covered

### Passage Planning Workflow
Complete pre-departure through execution workflow:
- Information gathering (almanacs, charts, weather, tides)
- Route planning with contingencies
- Safety equipment verification
- Shore contact establishment
- Leeway and tidal calculations
- ETA computation with safety margins
- Documentation requirements

### Safety Preparation
Systematic pre-departure safety procedures:
- Comprehensive safety briefing delivery
- Life jacket inspection and fitting
- Fire extinguisher verification
- Gas system safety checks
- Emergency equipment location
- Crew responsibility assignment
- Emergency procedure review

### Equipment Verification
Critical pre-departure equipment checks:
- Life jackets (bladder, gas bottle, crotch strap)
- Flares (seal integrity, expiration, quantity)
- Fire extinguishers (service dates, types, accessibility)
- Gas system (hoses, shut-offs, leak detection)
- Provisions (fuel 7/8 full, water 2L/person/day)
- Communications (VHF, DSC, EPIRB)

### Passage Calculations
Technical passage planning computations:
- Leeway allowances by vessel type
- Tidal stream effects on ETA
- Safety margins (15-30% buffer)
- "Latest arrival" time determination
- Fuel reserve calculations (20% minimum)
- Weather routing decisions

### Regulatory Compliance
Legal requirements for passage making:
- SOLAS V Regulation 34 (written passage plan required)
- Shore contact establishment (mandatory)
- Logbook documentation
- MAIB investigation requirements
- Evidence preservation

---

## 💡 Usage Examples

### Almanac Information Extraction
```
User: "What VHF channels for Cherbourg marina?"

Agent: Cherbourg Marina Information:

VHF Channels:
- Calling: Channel 09 (Cherbourg Port Control)
- Working: Channel 12 (Marina operations)
- Port Authority: Channel 16 (emergency monitoring)

Entry Notes:
- Monitor Ch 09 when entering harbor
- Switch to Ch 12 for berthing instructions
- Night entry: leading lights 078° (Fl.R.5s + Oc.G.6s)

High Water Time: +0015 on Cherbourg (Standard Port)
Lock Operating: HW ±2 hours (spring tides), HW ±3 hours (neaps)

Additional Info: Customs clearance available, fuel dock open 0800-2000
```

### Pre-Departure Safety Brief
```
User: "Run pre-departure safety brief"

Agent: ✅ PRE-DEPARTURE SAFETY BRIEFING

**Equipment Inspection Complete:**
✓ 6 life jackets inspected (all crotch straps functional)
✓ 8 flares checked (seals intact, expires 2027)
✓ 2 fire extinguishers serviced (AFFF + dry powder)
✓ Gas system verified (external locker, approved hoses)

**Crew Briefing Topics:**
1. Life Jacket Locations: Forward cabin lockers
2. Fire Extinguishers: Galley (AFFF) + companionway (dry powder)
3. MOB Equipment: Danbuoy + horseshoe + strobe aft pulpit
4. VHF Radio: Channel 16 monitoring, DSC MMSI: 235123456
5. EPIRB: Bracket on stern rail (registered to vessel)

**Emergency Procedures Reviewed:**
- MOB: "Mob! Mob! Mob!" + throw equipment + maintain visual
- Fire: NEVER open engine bay, discharge through access
- Mayday: DSC button + voice Channel 16 format
- Gas Leak: NO electrical switches, ventilate, locate source

**Shore Contact Established:**
- Contact: Jane Smith (mobile: +44 7700 900123)
- ETA: Alderney 1800 UTC
- Latest Arrival: 2100 UTC (raise alarm if no contact)
- Refuge Ports: Weymouth, Poole

Ready to depart? [Y/N]
```

### Passage Planning with Leeway
```
User: "Plan passage Brighton to Cherbourg, 25nm vessel, F4 SW wind"

Agent: 📋 PASSAGE PLAN: Brighton → Cherbourg

**Route:**
Distance: 70nm (Great Circle)
Course (True): 168°T
Magnetic: 167°M (Variation 1°W)

**Leeway Assessment:**
Vessel Type: 25nm cruising yacht (moderate windage)
Wind: F4 SW (on quarter)
Estimated Leeway: 5° (add 10-15% time allowance)

**Tidal Calculations:**
HW Dover: 1200 UTC
Stream Direction: Easterly (flood) 1200-1800
Stream Rate: 1.5kn average
Net Tidal Effect: +4nm westward drift over 6 hours

**ETA Computation:**
Base Time: 70nm ÷ 6kn = 11.7 hours
Leeway Allowance: +15% = 1.8 hours
Tidal Component: Accounted in course adjustment
Safety Margin: +20% = 2.6 hours
TOTAL TIME: 16.1 hours

Departure: 0600 UTC
ETA Cherbourg: 2206 UTC
**LATEST ARRIVAL: 0100 UTC (next day)**

**Shore Contact Package:**
Route: Brighton → Cherbourg (direct, 70nm)
Refuge Ports: Newhaven, Eastbourne, Shoreham (first 20nm)
Crew: 4 persons
Provisions: 36 hours
Safety Equipment: 6 life jackets, 8 flares, life raft, EPIRB
VHF: Channel 16 monitoring, DSC MMSI: 235123456

**Pre-Departure Checklist:**
□ Fuel: 180L (7/8 full, 40% reserve)
□ Water: 40L (2L/person/day + cooking)
□ Gas: Full bottle (10kg)
□ Provisions: 48 hours (including 33% reserve)
□ Weather: F4-5 SW, seas 1.5m, visibility good
□ Tides: Calculated for departure and arrival
□ Shore Contact: Informed (Latest Arrival: 0100)

SOLAS V Compliance: Written plan logged ✓

Ready to review weather and execute? [Y/N]
```

---

## 🎓 Teaching Methodology

### Systematic Approach
- **Six Ps of Passage Planning**: "Prior Preparation Prevents Piss Poor Performance"
- **SOLAS V Requirements**: Written passage plan mandatory
- **Rule of Three**: Three position fixes, three escape routes, three crew aware

### Safety-First Philosophy
- Pre-departure briefing is NON-NEGOTIABLE
- Shore contact with "latest arrival" time MANDATORY
- Equipment verification before EVERY passage
- Conservative safety margins in all calculations

### Practical Integration
- Combines chartwork, tidal calculations, weather analysis
- Realistic leeway assessment from vessel characteristics
- Shore contact establishment as legal requirement
- Documentation for MAIB investigation compliance

---

## 🔑 Critical Safety Principles

### Non-Negotiable Requirements
1. **Shore Contact Mandatory**: Always establish "latest arrival" time
2. **Life Jacket Crotch Straps**: Critical to prevent ride-up in water
3. **Engine Fire Protocol**: NEVER open bay (oxygen causes flashback)
4. **Gas Leak Response**: NO electrical switches (sparking risk)
5. **Flare Seal Integrity**: Damaged seals = useless flares
6. **Written Passage Plan**: SOLAS V legal requirement

### Equipment Inspection Intervals
- **Life Jackets**: Pre-departure visual inspection every trip
- **Flares**: Check expiration dates and seal integrity monthly
- **Fire Extinguishers**: Annual service, 5-year replacement
- **Gas Hoses**: Replace every 5 years regardless of condition
- **EPIRB**: Annual battery check, registration verification

### Leeway Considerations
- **High Windage Vessels**: Motor cruisers, high freeboard (greater leeway)
- **Deep Keel**: Reduced leeway due to lateral resistance
- **Light Winds**: Increased leeway (less water flow over foils)
- **Angle of Heel**: Greater heel = increased leeway
- **Reference Tables**: Build from wake bearing measurements

---

## 📚 Reference Materials

**Primary Sources:**
- `references/IMO_Passage_plan.pdf` - Official IMO passage planning standard
- `references/YachtMasterOffshoreSyllabus.txt` - RYA exam syllabus (Section 5 & 6)
- `references/YachtMasterOffshoreRequirements.txt` - Sea time and passage requirements

**Regulatory Framework:**
- SOLAS V Regulation 34: Voyage planning requirements
- MAIB (Marine Accident Investigation Branch): Investigation procedures
- RYA SafeTrx: Passage monitoring app

**Related Plugins:**
- **Plugin 01 (Chart Basics)**: Chart work and compass corrections
- **Plugin 02 (Tides)**: Tidal calculations for passage planning
- **Plugin 04 (Course to Steer)**: CTS calculations with leeway
- **Plugin 09 (Pilotage)**: Harbor entry techniques
- **Plugin 10 (Meteorology)**: Weather routing and forecasting

---

## 📊 Plugin Statistics

- **Skills**: 5 (passage planning workflow complete)
- **SOLAS V Compliance**: Full coverage
- **Safety Topics**: Pre-departure brief, LPG, fire, equipment verification
- **Passage Topics**: Almanac use, leeway calculation, shore contact, ETA computation

---

## 🎯 Learning Outcomes

After completing this plugin's skills, users will:

1. **Deliver comprehensive pre-departure safety briefings** to crew
2. **Verify all critical safety equipment** before departure
3. **Extract essential harbor information** from almanacs
4. **Calculate passage ETAs** with leeway and tidal effects
5. **Establish proper shore contacts** with "latest arrival" times
6. **Comply with SOLAS V** passage planning requirements
7. **Apply correct safety margins** (fuel, time, provisions)
8. **Execute LPG and fire safety protocols** correctly
9. **Document passages** for legal compliance
10. **Make go/no-go decisions** based on equipment readiness

---

## Version History

- **v1.6.0** (2025-11-10): Complete implementation with 5 skills (reorganization from Plugin 12)
- **v0.1.0** (2025-10-31): Initial plugin with almanac-navigator only

---

## Agent

See `agents/passage-making-tutor.md` for the complete Passage Making Tutor agent specification with detailed teaching approach and integration methodology.
