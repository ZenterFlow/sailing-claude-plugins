# Sailing Claude Plugins - Future Skills & Development Opportunities

## Executive Summary

This repository contains **14 sailing/navigation education plugins** organized as RYA/ASA YachtMaster training tools. Currently:

- **3 plugins** are feature-complete with implemented skills (Plugins 01, 02)
- **1 plugin** has partial implementation (Plugin 07-09)
- **10 plugins** are skeleton frameworks ready for skill development (Plugins 03-06, 10-14)

**Total Skills Implemented**: 17
**Total Future Skills Listed**: 23+

---

## Plugin Development Status by Number

### Plugin 01: Chart Basics ✅ COMPLETE
**Status**: Production Ready  
**Total Skills**: 8 implemented

**Implemented Skills**:
1. datum-guardian - GPS/chart datum compatibility
2. charted-height-interpreter - Vertical datum reference
3. symbol-spotter - Chart symbol interactive quiz (100+ symbols)
4. chart-correction-decoder - Read chart correction panels
5. corrections-mini-quiz - Correction reading quiz
6. chart-update-checklist - Hand-correction shopping list
7. chart-safe-go-nogo - Chart currency safety checks
8. photo-correction-reader - OCR chart correction photos

**Resources Available**:
- `datum-table.csv` - Geodetic datum reference data
- `symbols-deck.yml` - Chart symbol database (100+ symbols)
- Test suites for all skills
- Template files for datum calculations

**Topics Covered**:
- Geodetic datums (GPS ↔ Chart compatibility)
- Vertical datums (HAT, MHWS, CD, LAT, MSL)
- Chart symbols and abbreviations (INT 1 / 5011)
- Mercator projection principles
- Compass errors (variation & deviation)
- Chart corrections and currency (Notices to Mariners)

---

### Plugin 02: Tides ✅ COMPLETE
**Status**: Production Ready  
**Total Skills**: 5 implemented

**Implemented Skills**:
1. tide-calculator - Tidal height/time calculations (primary & secondary ports)
2. tidal-diamond-reader - Complete tidal diamond table display
3. diamond-dispatcher - Quick tidal diamond lookup by hour
4. depth-datum-flipper - Depth safety (UKC) and drying height calculations
5. vertical-clearance-solver - Bridge/overhead cable clearance checks

**Resources Available**:
- `datum-rules.yml` - Tidal datum reference rules
- Test suites with sample calculations
- Templates for tide calculations

**Topics Covered**:
- Tidal height calculations (primary & secondary ports)
- Tidal curves and rule-of-twelfths
- Tidal stream predictions and tidal diamonds
- Depth safety and under-keel clearance (UKC)
- Vertical clearance calculations
- Drying height conversions
- Irregular tides (Solent, Poole Harbour, etc.)

**Special Cases Documented**:
- Solent (double high water)
- Poole Harbour (complex patterns)
- Portland Bill (tidal races >5 knots)
- Victoria BC (mixed semi-diurnal tides)

---

### Plugin 03: Positioning 🚧 SKELETON
**Status**: Framework Only - No Skills Yet  
**Total Skills**: 0 implemented

**Future Skills Listed in Agent**:
1. visual-fix-calculator - Three-point bearing fixes, running fixes
2. ep-calculator - Estimated Position with leeway and tidal stream
3. cross-track-error-monitor - XTE tracking and monitoring
4. running-fix-plotter - Position line advancement calculations

**Topics Defined** (from agent file):
- Visual position fixing (compass bearings, ranges, transits)
- Three-point fix and running fix
- Estimated Position (EP) with leeway and tidal stream
- Dead Reckoning (DR) from course and speed
- Circle of error and fix accuracy
- Cross-track error (XTE)
- GPS position validation
- Position line advancement

**Implementation Priority**: HIGH
- These skills are fundamental to passage planning
- Heavy mathematical/calculation focus
- Templates available from related plugins (tides, course-to-steer)
- Agent has clear teaching methodology documented

---

### Plugin 04: Course to Steer 🚧 SKELETON
**Status**: Framework Only - No Skills Yet  
**Total Skills**: 0 implemented

**Future Skills Listed in Agent**:
1. cts-calculator - Course to Steer with leeway and stream vectors
2. velocity-triangle-plotter - Velocity triangle calculations and visualization

**Topics Defined** (from agent file):
- Course to Steer (CTS) calculations
- Leeway application (typically 5-10° downwind)
- Tidal stream vectors
- Velocity triangles (water triangle)
- Magnetic variation corrections
- Track made good vs course steered

**Implementation Priority**: HIGH
- Core navigation skill
- Closely related to Positioning (Plugin 03) and Tides (Plugin 02)
- Strong mathematical foundation exists in related plugins
- Could reuse datum/variation logic from Chart Basics

**Potential Resource Sharing**:
- Variation tables from Plugin 01 (datum-guardian)
- Tidal stream data from Plugin 02
- Mathematical templates for vector calculations

---

### Plugin 05: Electronic Navigation 🚧 SKELETON
**Status**: Framework Only - No Skills Yet  
**Total Skills**: 0 implemented

**Future Skills Listed in Agent**:
1. gps-accuracy-checker - GPS accuracy, HDOP, PDOP assessment
2. radar-range-calculator - Radar range ring calculations
3. ais-interpreter - AIS target symbol and data interpretation

**Topics Defined** (from agent file):
- GPS/GNSS principles and limitations
- Radar operation and interpretation
- AIS targets and symbols
- Electronic instruments (depth, speed, wind)
- Waypoint navigation
- MOB procedures using electronics
- SART and EPIRB

**Implementation Priority**: MEDIUM
- Less mathematically intense than positioning/course calculations
- More educational/explanatory in nature
- Could benefit from sample radar/AIS scenarios

---

### Plugin 06: Electronic Chart Plotting 🚧 SKELETON
**Status**: Framework Only - No Skills Yet  
**Total Skills**: 0 implemented

**Future Skills Listed in Agent**:
1. chart-plotter-validator - Validation against paper charts
2. enc-layer-explainer - ENC layer types and display options

**Topics Defined** (from agent file):
- ENC vs RNC chart types
- Chart plotter operation
- Route planning on plotters
- Alarm settings (XTE, depth, anchor)
- Chart updates and corrections
- Validation against paper charts
- ECDIS principles (commercial)

**Implementation Priority**: MEDIUM-HIGH
- Practical skill for modern navigation
- Related to chart corrections (Plugin 01) and chart validation

**Potential Resource Sharing**:
- Chart correction logic from Plugin 01
- ENC/RNC standards documentation needed

---

### Plugin 07: Passage Making ✅ PARTIAL
**Status**: 1 of many skills implemented  
**Total Skills**: 1 implemented

**Implemented Skills**:
1. almanac-navigator - Port info, VHF channels, HW differences, pilotage notes

**Resources Available**:
- `port-db.yml` - Port database with VHF channels, HW info
- Templates for port summaries

**Topics Covered**:
- Passage planning (pre-departure checks, waypoints, contingencies)
- Port information and facilities
- Watch systems and crew rotation
- Monitoring and log-keeping
- Weather windows and routing
- Safety briefings and emergency procedures

**Teaching Philosophy** (from agent):
- Six Ps of passage planning: "Prior Preparation Prevents Piss Poor Performance"
- SOLAS V requirements for passage plans
- Rule of three (three ways to fix, three escape routes, three crew)

**Future Skills Implied** (not explicitly listed):
- weather-routing-advisor (implied by "weather windows and routing" topic)
- log-keeper-template (implied by "monitoring and log-keeping")
- watch-system-planner (implied by "watch systems and crew rotation")
- passage-checklist-generator (implied by "pre-departure checks")

**Implementation Priority**: MEDIUM
- Current skill (almanac-navigator) is foundational
- Additional skills would support comprehensive passage planning

---

### Plugin 08: Visual Aids ✅ PARTIAL
**Status**: 1 of many skills implemented  
**Total Skills**: 1 implemented

**Implemented Skills**:
1. direction-of-buoyage-reminder - IALA A/B buoyage systems

**Topics Covered**:
- IALA A/B buoyage systems
- Lateral marks (port/starboard)
- Cardinal marks (N/E/S/W danger marking)
- Isolated danger and safe water marks
- Special marks (yellow)
- Light characteristics (Fl, Oc, Iso, Q, VQ, etc.)
- Ranges and transits
- Leading lines
- Dipping distance calculations

**Teaching Methodology** (from agent):
- Visual learner's best friend, pattern recognition focus
- Color coding and memory aids

**Future Skills Implied** (not explicitly listed):
- light-characteristics-quiz - Testing rhythm identification
- cardinal-marks-identifier - North/East/South/West marks with topmarks
- ranges-and-transits-guide - Leading line calculations
- dipping-distance-calculator - Line-of-sight range calculations

**Implementation Priority**: MEDIUM
- Well-structured visual content
- Builds on existing symbol/visual teaching approach from Plugin 01

---

### Plugin 09: Pilotage ✅ PARTIAL
**Status**: 2 of many skills implemented  
**Total Skills**: 2 implemented

**Implemented Skills**:
1. chart-update-checker - Verify chart currency and legality (SOLAS V)
2. almanac-navigator - Harbor entry notes, pilotage directions (shared with Plugin 07)

**Resources Available**:
- `port-db.yml` - Harbor-specific pilotage notes
- `nm-log.csv` - Notices to Mariners tracking log
- Templates for harbor entry procedures

**Topics Covered**:
- Pilotage planning (pre-approach preparation)
- Leading lines and transits
- Clearing bearings (danger bearings - NMT/NLT)
- Depth contour navigation
- Harbor entry procedures
- Restricted visibility techniques
- Traffic separation schemes (TSS)
- Port entry signals and VHF protocols

**Teaching Philosophy** (from agent):
- "Pilotage is navigation with consequences measured in boat lengths, not miles"
- Plan A, B, C + abort criteria clearly defined
- Conservative and thorough approach

**Future Skills Implied** (not explicitly listed):
- clearing-bearing-calculator - NMT/NLT danger bearing calculations
- leading-line-plotter - Transit and range calculations
- harbor-entry-planner - Pre-approach checklists
- restricted-visibility-navigator - Fog procedures and sound signals

**Implementation Priority**: HIGH
- Foundation skills already exist (chart-update-checker, almanac-navigator)
- Rich procedural content in agent file
- Clear teaching methodology for safety-critical skills

---

### Plugin 10: Meteorology 🚧 SKELETON
**Status**: Framework Only - No Skills Yet  
**Total Skills**: 0 implemented

**Future Skills Listed in Agent**:
1. synoptic-chart-reader - Pressure system interpretation
2. beaufort-scale-calculator - Wind/sea state assessment
3. weather-routing-advisor - Weather routing for passages

**Topics Defined** (from agent file):
- Weather forecast sources (GRIB, NAVTEX, VHF)
- Cloud types and what they mean
- Synoptic charts interpretation
- Pressure systems (highs, lows, fronts)
- Sea breeze effects
- Fog formation and types
- Beaufort scale
- Weather routing basics

**Implementation Priority**: MEDIUM
- More educational/explanatory rather than calculation-heavy
- Would benefit from sample synoptic charts and Beaufort scale data
- Could integrate with passage planning (Plugin 07)

**Potential Data Needs**:
- Beaufort scale lookup tables
- Synoptic chart symbols reference
- Cloud type identification guide

---

### Plugin 11: IRPCS ⚠️ SKELETON
**Status**: Framework Only - No Skills Yet  
**Total Skills**: 0 implemented

**Future Skills Listed in Agent**:
1. colreg-scenario-tester - Collision scenario analyzer
2. lights-and-shapes-quiz - Navigation lights and day shapes quiz
3. sound-signal-identifier - Fog signal identification

**Topics Defined** (from agent file):
- General rules (Rules 1-3: Application, Responsibility)
- Steering and sailing rules (Rules 4-19)
- Lights and shapes (Rules 20-31)
- Sound and light signals (Rules 32-37)
- Collision scenarios and case studies
- Special circumstances rule

**Implementation Priority**: MEDIUM-HIGH
- Heavily tested on RYA/ASA exams
- Clear rule-based structure (IRPCS/ColRegs)
- Overlaps with Plugin 14 (Nav Lights)

**Note**: Overlapping coverage with:
- Plugin 13 (Collision Regulations - Rules 11-18)
- Plugin 14 (Nav Lights Flip - navigation lights and day shapes)

---

### Plugin 12: Safety & Environment 🚧 SKELETON
**Status**: Framework Only - No Skills Yet  
**Total Skills**: 0 implemented

**Future Skills Listed in Agent**:
1. safety-brief-generator - Safety briefing templates
2. mayday-script-builder - Mayday and distress procedures
3. stability-calculator - Vessel stability calculations

**Topics Defined** (from agent file):
- Safety briefings and checklists
- Mayday and distress procedures
- GMDSS radio protocols
- Vessel stability principles
- Man overboard (MOB) procedures
- Fire fighting and damage control
- Environmental regulations (MARPOL)
- Waste disposal at sea

**Implementation Priority**: HIGH
- Safety-critical content
- Well-defined procedural content (Mayday, safety briefings)
- Could use template-based generation approach

**Potential Skills Expansion**:
- mob-procedure-guide (mentioned in topics but not listed)
- damage-control-planner (mentioned but not listed)
- gmdss-radio-guide (mentioned but not listed)

---

### Plugin 13: Collision Regulations 🚧 SKELETON
**Status**: Framework Only - No Skills Yet  
**Total Skills**: 0 implemented

**Future Skills Listed in Agent**:
1. collision-scenario-analyzer - Conduct analysis for Rules 11-18
2. right-of-way-calculator - Power/sailing vessel right-of-way determination

**Topics Defined** (from agent file):
- Conduct in sight (Rules 11-18)
- Power-driven vessels (head-on, crossing, overtaking)
- Sailing vessels (port/starboard tack, windward/leeward)
- Restricted visibility conduct (Rule 19)
- Responsibilities between vessels
- Action to avoid collision (early and substantial)

**Implementation Priority**: HIGH
- Heavily tested on RYA/ASA exams
- Clear scenario-based teaching potential
- Content overlaps with Plugin 11 but focuses on different rule sets

**Note**: Overlapping coverage with:
- Plugin 11 (IRPCS - which covers Rules 1-37)
- Plugin 14 (Nav Lights Flip - lights and shapes)

---

### Plugin 14: Nav Lights Flip Cards ✅ SKELETON (Quiz-Focused)
**Status**: Framework Only - No Skills Yet  
**Total Skills**: 0 implemented

**Future Skills Listed in Agent**:
1. lights-flashcard-quiz - Rapid-fire navigation lights quiz
2. shapes-identifier - Day shapes identification
3. sound-signal-quiz - Fog signal and maneuvering signals

**Topics Defined** (from agent file):
- Power vessel lights (underway, at anchor, aground)
- Sailing vessel lights
- Fishing vessel lights and shapes
- Towing and pushing configurations
- Pilot vessels, dredgers, diving operations
- Day shapes (ball, cone, diamond, cylinder)
- Sound signals (fog, maneuvering)
- Flag signals (A, B, O, etc.)

**Agent Identity**: "Quiz Master" - rapid-fire flashcard format

**Implementation Priority**: MEDIUM-HIGH
- Flashcard/quiz format is well-suited to agent capabilities
- Heavily tested content (RYA/ASA exams)
- Overlaps with Plugin 11 (IRPCS lights and shapes - Rules 20-31)

**Note**: Overlapping coverage with:
- Plugin 11 (IRPCS - Rules 20-31 cover lights and shapes)
- Plugin 13 (Collision Regulations - rules in sight)

---

## Skills Summary by Plugin

| Plugin | Name | Skills | Status | Future Skills | Priority |
|--------|------|--------|--------|----------------|----------|
| 01 | Chart Basics | 8 | ✅ Complete | None | N/A |
| 02 | Tides | 5 | ✅ Complete | None | N/A |
| 03 | Positioning | 0 | 🚧 Skeleton | 4 | HIGH |
| 04 | Course to Steer | 0 | 🚧 Skeleton | 2 | HIGH |
| 05 | Electronic Navigation | 0 | 🚧 Skeleton | 3 | MEDIUM |
| 06 | EC Plotting | 0 | 🚧 Skeleton | 2 | MEDIUM-HIGH |
| 07 | Passage Making | 1 | ⚠️ Partial | 3+ | MEDIUM |
| 08 | Visual Aids | 1 | ⚠️ Partial | 4+ | MEDIUM |
| 09 | Pilotage | 2 | ⚠️ Partial | 4+ | HIGH |
| 10 | Meteorology | 0 | 🚧 Skeleton | 3 | MEDIUM |
| 11 | IRPCS | 0 | 🚧 Skeleton | 3 | MEDIUM-HIGH |
| 12 | Safety & Environment | 0 | 🚧 Skeleton | 3 | HIGH |
| 13 | Collision Regulations | 0 | 🚧 Skeleton | 2 | HIGH |
| 14 | Nav Lights Flip | 0 | 🚧 Skeleton | 3 | MEDIUM-HIGH |

**Totals**:
- Implemented Skills: 17
- Future/Planned Skills: 23+
- Complete Plugins: 2
- Partial Plugins: 3
- Skeleton Plugins: 9

---

## Resource Files Available for Development

### Data Resources
- **datum-table.csv** (Plugin 01) - Geodetic datum shifts for major chart systems
- **symbols-deck.yml** (Plugin 01) - 100+ chart symbols with INT 1 references
- **datum-rules.yml** (Plugin 02) - Tidal datum conversion rules
- **port-db.yml** (Plugins 07, 09) - Port database with facilities, VHF channels, HW info
- **nm-log.csv** (Plugin 09) - Notices to Mariners tracking database

### Template Files
- **Port summary templates** (Plugins 07, 09)
- **Datum calculation templates** (Plugin 01)
- **Tidal calculation templates** (Plugin 02)
- **Chart correction templates** (Plugin 01)

### Test Suites
- All implemented skills have comprehensive test suites
- Sample prompts available for: tides, chart symbols, datum conversions, heights
- Test patterns can be replicated for new skills

---

## Recommended Implementation Roadmap

### Phase 1: Core Navigation Foundation (HIGH PRIORITY)
1. **Plugin 03 - Positioning Skills** (4 skills)
   - visual-fix-calculator
   - ep-calculator
   - cross-track-error-monitor
   - running-fix-plotter
   - *Rationale*: Fundamental to all navigation; heavy template/calculation work

2. **Plugin 04 - Course to Steer Skills** (2 skills)
   - cts-calculator
   - velocity-triangle-plotter
   - *Rationale*: Core calculation skill; closely related to Positioning

### Phase 2: Advanced Navigation & Safety (HIGH PRIORITY)
3. **Plugin 09 - Pilotage Skills** (remaining 4+)
   - clearing-bearing-calculator
   - leading-line-plotter
   - harbor-entry-planner
   - restricted-visibility-navigator
   - *Rationale*: Safety-critical; foundation skills already exist

4. **Plugin 12 - Safety & Environment** (3 skills)
   - safety-brief-generator (template-based)
   - mayday-script-builder (procedural)
   - stability-calculator (calculation-based)
   - *Rationale*: Safety-critical content with clear procedures

### Phase 3: Rules & Regulations (MEDIUM-HIGH PRIORITY)
5. **Plugin 13 - Collision Regulations** (2 skills)
   - collision-scenario-analyzer
   - right-of-way-calculator
   - *Rationale*: Heavily tested; scenario-based content

6. **Plugin 11 & 14 - Rules & Lights** (6 skills)
   - Plugin 11: colreg-scenario-tester, lights-and-shapes-quiz, sound-signal-identifier
   - Plugin 14: lights-flashcard-quiz, shapes-identifier, sound-signal-quiz
   - *Rationale*: Quiz/flashcard format suits agent capabilities; heavily tested

### Phase 4: Electronic Navigation & Systems (MEDIUM PRIORITY)
7. **Plugin 05 - Electronic Navigation** (3 skills)
   - gps-accuracy-checker
   - radar-range-calculator
   - ais-interpreter

8. **Plugin 06 - Electronic Chart Plotting** (2 skills)
   - chart-plotter-validator
   - enc-layer-explainer

### Phase 5: Supplementary Skills (MEDIUM PRIORITY)
9. **Plugin 07 - Passage Making** (additional skills)
   - weather-routing-advisor
   - log-keeper-template
   - watch-system-planner

10. **Plugin 08 - Visual Aids** (additional skills)
    - light-characteristics-quiz
    - cardinal-marks-identifier
    - ranges-and-transits-guide
    - dipping-distance-calculator

11. **Plugin 10 - Meteorology** (3 skills)
    - synoptic-chart-reader
    - beaufort-scale-calculator
    - weather-routing-advisor

---

## Cross-Plugin Dependencies & Opportunities

### Strong Dependencies
- **Plugin 03 ← Plugin 02**: Positioning uses tidal streams
- **Plugin 04 ← Plugins 01, 02, 03**: CTS uses variation, tides, and positioning
- **Plugin 07 ← Plugins 02, 03, 04**: Passage making requires tide, position, and CTS
- **Plugin 09 ← Plugins 01, 02, 07**: Pilotage requires charts, tides, and passage planning

### Resource Sharing Opportunities
- **Variation tables** from Plugin 01 can serve Plugins 04, 07, 09
- **Tidal stream data** from Plugin 02 can serve Plugins 03, 04, 07
- **Port database** from Plugins 07/09 can enhance Plugin 10 (weather routing)
- **Chart symbols** from Plugin 01 foundational for Plugins 06, 09
- **Vector calculation templates** from Plugins 02, 04 reusable for Plugin 05

### Teaching Synergies
- Plugins 11, 13, 14 all teach collision avoidance rules (coordinated coverage)
- Plugins 01, 06, 09 all involve chart work (visual/systematic approach)
- Plugins 02, 03, 04 form a progression: tides → positioning → course calculation

---

## Skill Implementation Complexity Guide

### High Complexity (Calculation-Heavy)
- Plugin 03: visual-fix-calculator, ep-calculator
- Plugin 04: cts-calculator, velocity-triangle-plotter
- Plugin 02: All 5 skills (already implemented)
- Plugin 05: radar-range-calculator
- Plugin 10: beaufort-scale-calculator

### Medium Complexity (Rule-Based)
- Plugin 13: collision-scenario-analyzer, right-of-way-calculator
- Plugin 11: colreg-scenario-tester
- Plugin 06: enc-layer-explainer
- Plugin 05: gps-accuracy-checker, ais-interpreter

### Lower Complexity (Quiz/Template-Based)
- Plugin 14: lights-flashcard-quiz, shapes-identifier, sound-signal-quiz
- Plugin 08: light-characteristics-quiz, cardinal-marks-identifier
- Plugin 11: lights-and-shapes-quiz, sound-signal-identifier
- Plugin 12: safety-brief-generator, mayday-script-builder
- Plugin 07: watch-system-planner, log-keeper-template

---

## Notes for Prioritization

1. **Exam Coverage**: Plugins 01-04, 11, 13-14 are heavily tested on RYA YachtMaster exam
2. **Foundation Skills**: Plugins 01, 02, 03, 04 form the mathematical foundation
3. **Safety-Critical**: Plugins 09, 12, 13 require extra attention to accuracy
4. **Quick Wins**: Plugin 14 (flashcard quizzes) likely easiest to implement
5. **Resource Availability**: Plugins 01, 02 show good patterns for structuring new skills
6. **Overlapping Content**: Plugins 11, 13, 14 should be coordinated to avoid duplication
