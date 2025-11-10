# Sailing Claude Plugins - Future Skills & Development Opportunities

## Executive Summary

This repository contains **14 sailing/navigation education plugins** organized as RYA/ASA YachtMaster training tools. Currently:

- **8 plugins** are feature-complete with implemented skills (Plugins 01, 02, 03, 04, 05, 06, 08, 09)
- **1 plugin** has partial implementation (Plugin 07)
- **5 plugins** are skeleton frameworks ready for skill development (Plugins 10-14)

**Total Skills Implemented**: 81
**Total Future Skills Listed**: 0 (all core navigation skills complete)

---

## Plugin Development Status by Number

### Plugin 01: Chart Basics ✅ COMPLETE
**Status**: Production Ready (100% RYA/ASA chart basics syllabus)
**Total Skills**: 17 implemented

**Implemented Skills**:
1. datum-guardian - GPS/chart datum compatibility
2. charted-height-interpreter - Vertical datum reference
3. longitude-latitude - Lat/long scale reading
4. chartwork-mercator-projection - Mercator projection principles
5. symbol-spotter - Chart symbol interactive quiz (100+ symbols)
6. symbol-quiz-flashcards - Rapid-fire flashcard quiz
7. chart-symbol-spotter - Symbol identification by name/photo
8. chart-correction-decoder - Read chart correction panels
9. corrections-mini-quiz - Correction reading quiz
10. chart-update-checklist - Hand-correction shopping list
11. chart-update-checker - Verify chart currency
12. chart-safe-go-nogo - Chart currency safety checks
13. photo-correction-reader - OCR chart correction photos
14. magnetic-variation-calculator - Calculate variation from compass rose (NEW v0.5.0)
15. compass-error-corrector - T ↔ M ↔ C conversions with CADET (NEW v0.5.0)
16. deviation-table-reader - Read and interpolate deviation tables (NEW v0.5.0)
17. hand-bearing-compass-guide - Position fixing and collision avoidance (NEW v0.5.0)

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
**Status**: Production Ready (v0.6.0)
**Total Skills**: 8 implemented

**Implemented Skills**:
1. tide-calculator - Tidal height/time calculations (primary & secondary ports)
2. tidal-diamond-reader - Complete tidal diamond table display
3. diamond-dispatcher - Quick tidal diamond lookup by hour
4. depth-datum-flipper - Depth safety (UKC) and drying height calculations
5. vertical-clearance-solver - Bridge/overhead cable clearance checks
6. tidal-terminology-guide - Vertical datums (HAT, MHWS, CD, LAT) (NEW v0.6.0)
7. time-zone-converter - UT/maritime zone/DST conversions (NEW v0.6.0)
8. tidal-theory-explainer - Astronomical causes of tides, spring/neap cycles (NEW v0.6.0)

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

### Plugin 03: Positioning ✅ COMPLETE
**Status**: Production Ready (v0.4.0)
**Total Skills**: 8 implemented

**Implemented Skills**:
1. visual-fix-calculator - Three-point bearing fixes, running fixes, cocked hat assessment
2. ep-calculator - Estimated Position and Dead Reckoning with leeway and tidal stream
3. cross-track-error-monitor - XTE calculation and monitoring for TSS and channels
4. visual-fix-reliability - Assess visual fix quality and reliability using cocked hat analysis
5. enhanced-visual-fixing - Advanced visual fixing techniques (running fixes, four-point fixes)
6. position-fix-integrator - Complete position fixing workflow integration
7. navigation-web-constructor - Pre-plotted bearing/distance grids for rapid GPS monitoring (NEW v0.9.0)
8. angle-off-bow-fix - Quick distance-off using 45°/90° relative bearing method (NEW v0.9.0)

**Topics Defined** (from agent file):
- Visual position fixing (compass bearings, ranges, transits)
- Three-point fix and running fix
- Estimated Position (EP) with leeway and tidal stream
- Dead Reckoning (DR) from course and speed
- Circle of error and fix accuracy
- Cross-track error (XTE)
- GPS position validation
- Position line advancement

**Resources Available**:
- Complete calculation templates for visual fixes, EP, and XTE
- Bearing geometry guides and leeway estimation tables
- TSS requirements and XTE monitoring procedures
- Comprehensive test suites

**Topics Fully Covered**:
- Visual position fixing with three-point and running fixes
- Estimated Position with leeway and tidal stream
- Dead Reckoning calculations
- Cross-track error monitoring for TSS navigation
- Cocked hat assessment and fix quality evaluation

---

### Plugin 04: Course to Steer ✅ COMPLETE
**Status**: Production Ready (v0.3.0)
**Total Skills**: 7 implemented

**Implemented Skills**:
1. cts-calculator - Course To Steer calculations with leeway, stream, and magnetic corrections
2. velocity-triangle-plotter - Graphical velocity triangle solutions for CTS and TMG problems
3. vector-triangle-plotter - Complete CTS vector triangle plotting on chart (NEW v0.3.0)
4. leeway-applicator - Apply leeway correction to True CTS (port/starboard tack rules) (NEW v0.3.0)
5. multi-factor-converter - Complete T→M→C conversion sequence with variation and deviation (NEW v0.3.0)
6. tidal-hour-selector - Determine correct tidal hour for CTS based on trip timing (NEW v0.3.0)
7. cts-practical-integrator - Complete end-to-end CTS workflow integration (NEW v0.3.0)

**Topics Defined** (from agent file):
- Course to Steer (CTS) calculations
- Leeway application (typically 5-10° downwind)
- Tidal stream vectors
- Velocity triangles (water triangle)
- Magnetic variation corrections
- Track made good vs course steered

**Resources Available**:
- Complete CTS calculation methods with vector solutions
- Velocity triangle plotting templates and diagrams
- Step-by-step worked examples
- Comprehensive test suites

**Topics Fully Covered**:
- Course To Steer with leeway and tidal stream
- Velocity triangle construction and interpretation
- Magnetic variation and deviation corrections
- Track made good vs course steered calculations
- Speed over ground estimation

---

### Plugin 05: Electronic Navigation ✅ COMPLETE
**Status**: Production Ready (v0.8.0)
**Total Skills**: 16 implemented

**Implemented Skills**:
1. gps-gnss-fundamentals - GPS/GNSS principles, HDOP, accuracy metrics
2. gps-data-interpretation - SOG, COG, XTE, TTG, VMG data interpretation
3. depth-sounder-configuration - Offset calibration (keel, waterline, transducer)
4. radar-basics-limitations - Radar principles, beam width, range vs bearing accuracy
5. ais-target-interpretation - AIS symbols, CPA/TCPA, target classification
6. integrated-electronic-navigation - Multi-system integration and cross-checking
7. electronic-navigation-limitations - System limitations and backup procedures
8. waypoint-management-safety - Safe waypoint placement and entry validation
9. navigation-instrument-calibration - Log, depth, and wind instrument calibration
10. radar-pilotage-techniques - Radar fixes, parallel indexing, clearing ranges
11. marpa-collision-assessment - MARPA target tracking and CPA/TCPA interpretation
12. electronic-navigation-integration - Comprehensive system integration with paper chart backup (NEW v0.8.0)
13. radar-overlay-verification - Position verification using radar overlay in fog (NEW v0.8.0)
14. feature-radar-appearance - Predict how coastal features appear on radar (NEW v0.8.0)
15. restricted-visibility-decision - Fog navigation continue/stand-off decision making (NEW v0.8.0)
16. ais-data-source-distinction - Direct VHF vs internet AIS data comparison (NEW v0.8.0)

**Topics Covered**:
- GPS/GNSS principles and limitations
- Radar operation and interpretation
- AIS targets and symbols
- Electronic instruments (depth, speed, wind)
- Waypoint navigation
- MOB procedures using electronics
- SART and EPIRB

---

### Plugin 06: Electronic Chart Plotting ✅ COMPLETE
**Status**: Production Ready (v0.8.0)
**Total Skills**: 5 implemented

**Implemented Skills**:
1. electronic-chart-types - RNC vs ENC comparison, quality indicators, limitations
2. chart-plotter-operation - Menu navigation, alarm configuration, safety settings
3. auto-route-verification - Verify auto-routed courses against paper charts and warning icons (NEW v0.8.0)
4. mobile-device-repeater - Use tablets/phones as plotter repeaters with understanding of limitations (NEW v0.8.0)
5. waypoint-positioning-adjustment - Adjust waypoints for fog navigation using depth contours (NEW v0.8.0)

**Topics Covered**:
- ENC vs RNC chart types
- Chart plotter operation
- Route planning on plotters
- Alarm settings (XTE, depth, anchor)
- Chart updates and corrections
- Validation against paper charts
- ECDIS principles (commercial)

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

### Plugin 08: Visual Aids ✅ COMPLETE
**Status**: Production Ready (v1.0.0)
**Total Skills**: 11 implemented

**Implemented Skills**:
1. iala-buoyage-system - IALA Region A/B fundamentals, direction of buoyage, five mark categories (NEW v1.0.0)
2. lateral-marks-identifier - Port and starboard marks with regional color variations and preferred channel indicators (NEW v1.0.0)
3. cardinal-marks-identifier - N/E/S/W cardinal marks identification
4. special-purpose-marks - Isolated danger, safe water, special marks, and wreck markers (NEW v1.0.0)
5. light-characteristics-quiz - Interactive quiz for navigation lights
6. light-ranges-beacons - Geographical/luminous/nominal ranges, dipping distance, RACON identification (NEW v1.0.0)
7. admiralty-list-lights - Extract and interpret Admiralty List of Lights and navigation publications (NEW v1.0.0)
8. ranges-and-transits-guide - Visual position fixing with ranges and transits
9. dipping-distance-calculator - Geographic range calculations
10. direction-of-buoyage-reminder - Quick reference for IALA buoyage rules
11. visual-aids-quiz - Rapid identification quiz covering all navigation marks (NEW v1.0.0)

**Topics Fully Covered**:
- IALA A/B regional differences and direction of buoyage
- Lateral marks with regional color variations (port/starboard)
- Preferred channel indicators (2+1 light pattern)
- Cardinal marks (N/E/S/W danger marking) with topmark recognition
- Isolated danger marks (black/red bands, two balls)
- Safe water marks (red/white vertical stripes)
- Special marks (yellow with X topmark)
- Temporary wreck markers (blue/yellow stripes)
- Light characteristics (Fl, Oc, Iso, Q, VQ, UQ, LFl, Morse)
- Geographical vs luminous vs nominal light ranges
- Dipping distance calculations (2.08√h formula)
- Sector lights and moire lights
- RACON identification on radar
- Admiralty List of Lights usage and updates
- Notices to Mariners corrections
- Ranges and transits for position fixing
- Leading lines and lights
- Comprehensive visual aids identification

**Teaching Methodology**:
- Visual learner's best friend, pattern recognition focus
- Color coding and memory aids
- Interactive quizzes

---

### Plugin 09: Pilotage ✅ COMPLETE
**Status**: Production Ready (v1.1.0)
**Total Skills**: 13 implemented

**Implemented Skills**:
1. pilotage-fundamentals - Core concept: visible objects avoid invisible dangers, information sources (NEW v1.1.0)
2. chart-update-checker - Verify chart currency and legality (SOLAS V)
3. leading-lines-transit - Charted transits, leading lights, lower light rule, compass deviation checks (NEW v1.1.0)
4. clearing-bearings - NMT/NLT danger bearings for safe corridors between hazards (NEW v1.1.0)
5. moire-lights - Precise bridge and entrance alignment with directional narrow-sector lights (NEW v1.1.0)
6. pilotage-planning - Create pictorial and rolling road plans for deck execution (NEW v1.1.0)
7. almanac-navigator - Harbor entry notes, pilotage directions (shared with Plugin 07)
8. harbor-entry-planner - Plan A/B/C with abort criteria
9. restricted-visibility - Fog pilotage using depth contours, radar, GPS with proper watchkeeping (NEW v1.1.0)
10. leading-line-plotter - Transit range calculations and position fixing
11. integrated-pilotage - Synthesize all techniques into comprehensive passage plans (NEW v1.1.0)
12. clearing-bearing-calculator - Calculate and verify clearing bearing corridors
13. restricted-visibility-navigator - COLREGS fog procedures and sound signals

**Resources Available**:
- `port-db.yml` - Harbor-specific pilotage notes
- `nm-log.csv` - Notices to Mariners tracking log
- Templates for harbor entry procedures

**Topics Fully Covered**:
- Pilotage fundamentals (visible objects to avoid invisible dangers)
- Information sources (almanacs, pilot books, charts)
- GPS limitations and cockpit navigation
- Variation application (True to Magnetic conversion)
- Leading lines and charted transits (magenta lines)
- Leading lights operation and lower light rule (universal)
- Clearing bearings (NMT/NLT danger bearing corridors)
- Improvised transits from charted objects
- Compass deviation checks using known transits
- Moire lights for precise bridge/entrance alignment
- Pictorial/sketch plans (bird's eye view format)
- Rolling road plans and tram lines (linear track format)
- Required information checklist (tides, ports, visual aids, routes)
- Standard leg format specification
- Chart protection (never take originals on deck)
- Hand bearing compass continuous monitoring
- Depth contour navigation and following
- Tacking at clearing bearing limits
- Night pilotage with entrance lights
- Visual verification at waypoints
- Height of Tide (HOT) calculations and application
- Fog pilotage using depth contours (primary method)
- 10% circle of error rule for buoy location
- Radar and GPS as secondary navigation tools
- Proper watchkeeping discipline (all available means)
- COLREGS fog signals (Rule 35)
- Buoy search patterns on depth contours
- Comprehensive passage plans (open water to mooring)
- Multiple technique synthesis in single plan
- Tidal height integration throughout passage
- Hazard avoidance strategy combinations
- Contingency planning for all critical legs
- Night departures from anchorage with multiple routes
- Plan execution discipline (cockpit-based, when in doubt stop)
- Chart currency requirements (SOLAS V Regulation 19)
- Port entry protocols and VHF communications
- Traffic separation scheme (TSS) navigation
- Emergency procedures (if lost, if uncertain)
- Abort criteria definition before approach

**Teaching Philosophy** (from agent):
- "Pilotage is navigation with consequences measured in boat lengths, not miles"
- Plan A, B, C + abort criteria clearly defined
- Conservative and thorough approach

**Topics Fully Covered**:
- Clearing bearings (NMT/NLT) for danger avoidance
- Leading lines and transits for safe passage
- Harbor entry planning with contingencies
- Restricted visibility procedures (fog, COLREGS Rule 19 & 35)
- Chart currency verification
- Pilotage notes and harbor-specific information

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
| 01 | Chart Basics | 17 | ✅ Complete | None | N/A |
| 02 | Tides | 8 | ✅ Complete | None | N/A |
| 03 | Positioning | 8 | ✅ Complete | None | N/A |
| 04 | Course to Steer | 7 | ✅ Complete | None | N/A |
| 05 | Electronic Navigation | 16 | ✅ Complete | None | N/A |
| 06 | EC Plotting | 5 | ✅ Complete | None | N/A |
| 07 | Passage Making | 1 | ⚠️ Partial | 3+ | MEDIUM |
| 08 | Visual Aids | 5 | ✅ Complete | None | N/A |
| 09 | Pilotage | 6 | ✅ Complete | None | N/A |
| 10 | Meteorology | 0 | 🚧 Skeleton | 3 | MEDIUM |
| 11 | IRPCS | 0 | 🚧 Skeleton | 3 | MEDIUM-HIGH |
| 12 | Safety & Environment | 0 | 🚧 Skeleton | 3 | HIGH |
| 13 | Collision Regulations | 0 | 🚧 Skeleton | 2 | HIGH |
| 14 | Nav Lights Flip | 0 | 🚧 Skeleton | 3 | MEDIUM-HIGH |

**Totals**:
- Implemented Skills: 68
- Future/Planned Skills: 10+ (remaining)
- Complete Plugins: 8 (Plugins 01, 02, 03, 04, 05, 06, 08, 09)
- Partial Plugins: 1 (Plugin 07)
- Skeleton Plugins: 5 (Plugins 10, 11, 12, 13, 14)

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

### ✅ Phase 1: Core Navigation Foundation (COMPLETED - v0.2.0)
1. **Plugin 03 - Positioning Skills** ✅ DONE
   - ✅ visual-fix-calculator
   - ✅ ep-calculator
   - ✅ cross-track-error-monitor

2. **Plugin 04 - Course to Steer Skills** ✅ DONE
   - ✅ cts-calculator
   - ✅ velocity-triangle-plotter

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
