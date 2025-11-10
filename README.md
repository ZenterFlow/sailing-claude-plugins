# ⛵ Sailing Curriculum – Claude Plugin Marketplace

**One-command access to the full RYA/ASA navigation syllabus inside Claude Code.**

This plugin suite provides 14 specialized agents with dedicated skills, turning your Claude Code environment into a comprehensive, interactive tutor for sailing navigation and theory.

---

## 🚀 Installation

### Step 1: Add the Marketplace

```bash
/plugin marketplace add ZenterFlow/sailing-claude-plugins
```

### Step 2: Install Individual Plugins

Install the plugins you need:

```bash
# Ready for testing (with implemented skills)
/plugin install chart-basics@sailing-curriculum
/plugin install tides@sailing-curriculum
/plugin install positioning@sailing-curriculum
/plugin install course-to-steer@sailing-curriculum
/plugin install electronic-navigation@sailing-curriculum
/plugin install ec-plotting@sailing-curriculum
/plugin install passage-making@sailing-curriculum
/plugin install visual-aids@sailing-curriculum
/plugin install pilotage@sailing-curriculum

# In development (skeleton agents, no skills yet)
/plugin install meteorology@sailing-curriculum
# ... and 4 more
```

### Or Install All at Once

```bash
# Install all 14 plugins
/plugin install chart-basics@sailing-curriculum && \
/plugin install tides@sailing-curriculum && \
/plugin install positioning@sailing-curriculum && \
/plugin install course-to-steer@sailing-curriculum && \
/plugin install electronic-navigation@sailing-curriculum && \
/plugin install ec-plotting@sailing-curriculum && \
/plugin install passage-making@sailing-curriculum && \
/plugin install visual-aids@sailing-curriculum && \
/plugin install pilotage@sailing-curriculum && \
/plugin install meteorology@sailing-curriculum && \
/plugin install irpcs@sailing-curriculum && \
/plugin install safety-environment@sailing-curriculum && \
/plugin install collision-regs@sailing-curriculum && \
/plugin install nav-lights-flip@sailing-curriculum
```

### Verify Installation

```bash
/plugin
```

This opens the interactive plugin management interface where you can see all installed plugins.

---

## 📚 The 14 Topic Agents

Each plugin contains:
- **One specialized tutor agent** with expertise in that topic
- **Multiple skills** that the agent uses to teach and assist
- **Interactive examples** and worked calculations
- **RYA/ASA exam-focused** content

### ✅ Ready for Testing (10 plugins, 87 skills)

| Plugin | Agent | Skills | Status |
|--------|-------|--------|--------|
| **01. Chart Basics** | Chart Basics Tutor | 17 skills: datum-guardian, charted-height-interpreter, longitude-latitude, chartwork-mercator-projection, symbol-spotter, symbol-quiz-flashcards, chart-symbol-spotter, chart-correction-decoder, corrections-mini-quiz, chart-update-checklist, chart-update-checker, chart-safe-go-nogo, photo-correction-reader, magnetic-variation-calculator, compass-error-corrector, deviation-table-reader, hand-bearing-compass-guide | ✅ Complete |
| **02. Tides** | Tides Tutor | 8 skills: tide-calculator, tidal-diamond-reader, diamond-dispatcher, depth-datum-flipper, vertical-clearance-solver, tidal-terminology-guide, time-zone-converter, tidal-theory-explainer | ✅ Complete |
| **03. Positioning** | Positioning Tutor | 8 skills: visual-fix-calculator, ep-calculator, cross-track-error-monitor, visual-fix-reliability, enhanced-visual-fixing, position-fix-integrator, navigation-web-constructor, angle-off-bow-fix | ✅ Complete |
| **04. Course to Steer** | Course to Steer Tutor | 7 skills: cts-calculator, velocity-triangle-plotter, vector-triangle-plotter, leeway-applicator, multi-factor-converter, tidal-hour-selector, cts-practical-integrator | ✅ Complete |
| **05. Electronic Nav** | Electronic Navigation Tutor | 16 skills: gps-gnss-fundamentals, gps-data-interpretation, depth-sounder-configuration, radar-basics-limitations, ais-target-interpretation, integrated-electronic-navigation, electronic-navigation-limitations, waypoint-management-safety, navigation-instrument-calibration, radar-pilotage-techniques, marpa-collision-assessment, electronic-navigation-integration, radar-overlay-verification, feature-radar-appearance, restricted-visibility-decision, ais-data-source-distinction | ✅ Complete |
| **06. EC Plotting** | EC Plotting Tutor | 5 skills: electronic-chart-types, chart-plotter-operation, auto-route-verification, mobile-device-repeater, waypoint-positioning-adjustment | ✅ Complete |
| **07. Passage Making** | Passage Making Tutor | 1 skill: almanac-navigator | ✅ Ready |
| **08. Visual Aids** | Visual Aids Tutor | 11 skills: iala-buoyage-system, lateral-marks-identifier, cardinal-marks-identifier, special-purpose-marks, light-characteristics-quiz, light-ranges-beacons, admiralty-list-lights, ranges-and-transits-guide, dipping-distance-calculator, direction-of-buoyage-reminder, visual-aids-quiz | ✅ Complete |
| **09. Pilotage** | Pilotage Tutor | 13 skills: pilotage-fundamentals, chart-update-checker, leading-lines-transit, clearing-bearings, moire-lights, pilotage-planning, almanac-navigator, harbor-entry-planner, restricted-visibility, leading-line-plotter, integrated-pilotage, clearing-bearing-calculator, restricted-visibility-navigator | ✅ Complete |
| **10. Meteorology** | Meteorology Tutor | 6 skills: meteorology-fundamentals, global-weather-systems, weather-interactions, cloud-types, local-weather-fog, pressure-forecast-application | ✅ Complete |

### 🚧 In Development (4 plugins)

| Plugin | Agent | Topics Covered |
|--------|-------|----------------|
| **11. IRPCS** | IRPCS Tutor | Collision regulations, rules, case studies |
| **12. Safety & Environment** | Safety & Environment Tutor | Safety briefs, Mayday, stability, MARPOL |
| **13. Collision Regs** | Collision Regs Tutor | Conduct in sight, restricted visibility |
| **14. Nav Lights Flip** | Nav Lights Quiz Master | Lights, shapes, signals flashcard quiz |

---

## 💡 Usage Examples

The agents auto-trigger when you ask relevant questions:

### Chart Basics (Plugin 01)
```
User: Can I plot WGS-84 onto BA 2454?

Agent: ✅ SAFE TO PLOT
BA 2454 uses WGS-84 geodetic datum.
Your GPS is also WGS-84.
→ No shift required - plot position directly.
```

### Tides (Plugin 02)
```
User: What's the tide at 14:30 at Portsmouth on June 15?

Agent: Let me calculate...
HW: 11:25 UTC at 4.7m CD
LW: 17:50 UTC at 1.2m CD
At 14:30: 2.5m above Chart Datum
[Shows full workings with tidal curve]
```

### Tidal Safety (Plugin 02)
```
User: Draught 1.8m, chart 3.2m, tide 2.1m. Am I safe?

Agent: Available: 3.2 + 2.1 = 5.3m
Required: 1.8 + 0.5 = 2.3m
✅ SAFE - Clearance: 3.0m
Actual UKC: 3.5m (well above minimum)
```

### Chart Symbols Quiz (Plugin 01)
```
User: Test me on chart symbols

Agent: 🎯 CHART SYMBOL QUIZ - Question 1/10
What does this symbol mean?
    ⚓ (3)
A) Anchorage, maximum depth 3m
B) Anchor prohibited, 3 cables radius
C) Anchorage, depth 3 fathoms
D) Anchoring area, 3 vessels max
```

### Tidal Stream (Plugin 02)
```
User: Diamond F at HW+3, spring tides

Agent: SET: 245°T (WSW)
DRIFT: 2.8 knots
Apply for ±1 hour either side of HW+3
[Includes application notes for EP/CTS]
```

---

## 🎯 Plugin Details

### Plugin 01: Chart Basics ✅
**Topics**: Chart datum, symbols, Mercator projection, compass errors, chart corrections
**Skills** (8 total):
- datum-guardian (GPS ↔ chart datum shifts)
- charted-height-interpreter (HAT, MHWS, CD, LAT datums)
- symbol-spotter (100+ chart symbols quiz)
- chart-correction-decoder (Read and explain correction panels)
- corrections-mini-quiz (Interactive quiz on chart corrections)
- chart-update-checklist (How to update charts with magenta pen)
- chart-safe-go-nogo (Determine if chart is current enough)
- photo-correction-reader (OCR correction panels from photos)

**Triggers**: "datum shift", "chart symbol", "variation and deviation", "WGS-84 vs ED-50", "chart correction", "Notice to Mariners"

---

### Plugin 02: Tides ✅
**Topics**: Tide calculations, streams, diamonds, depth/clearance safety
**Skills**:
- tide-calculator (Heights/times, primary/secondary ports, twelfths)
- tidal-diamond-reader (Full diamond tables)
- diamond-dispatcher (Quick diamond lookup)
- depth-datum-flipper (UKC checks, drying heights)
- vertical-clearance-solver (Bridge clearances)

**Triggers**: "tide height", "will I touch", "bridge clearance", "drying height", "diamond F HW+3"

---

### Plugin 07: Passage Making ✅
**Topics**: Planning, port info, watch systems, monitoring
**Skills**:
- almanac-navigator (Port info, VHF channels, pilotage notes)

**Triggers**: "port information", "HW difference", "VHF channels", "pilotage directions"

---

### Plugin 08: Visual Aids ✅
**Topics**: Buoys, lights, ranges, transits, IALA system
**Skills**:
- direction-of-buoyage-reminder (Which side to leave buoys)

**Triggers**: "direction of buoyage", "IALA", "red or green buoy", "leave port or starboard"

---

### Plugin 09: Pilotage ✅
**Topics**: Harbor entry, leading lines, clearing bearings, chart updating
**Skills**:
- chart-update-checker (Verify charts are current/legal)
- almanac-navigator (Harbor entry notes)

**Triggers**: "harbor entry", "chart updates", "is my chart current", "NM to apply"

---

## 🏗️ Architecture

Each plugin follows the official Claude Code plugin structure:

```
NN-plugin-name/
├── .claude-plugin/
│   └── plugin.json         # Required metadata (name, version, author)
├── agents/
│   └── tutor-name.md       # Agent personality and teaching approach
├── skills/                 # Individual skills (for plugins with skills)
│   ├── skill-name/
│   │   ├── SKILL.md        # Skill description and behavior
│   │   ├── manifest.json   # Skill metadata
│   │   ├── instructions.md # Detailed instructor notes
│   │   ├── resources/      # Reference data (CSV, YAML, images)
│   │   ├── templates/      # Reusable response templates
│   │   └── tests/          # Sample prompts for validation
│   └── another-skill/
│       └── ...
├── plugin.md               # Comprehensive documentation (where applicable)
└── README.md               # Quick plugin overview
```

**Marketplace Structure**:
```
sailing-claude-plugins/
├── .claude-plugin/
│   └── marketplace.json    # Marketplace catalog (14 plugins)
├── 01-chart-basics/
├── 02-tides/
├── ... (12 more plugins)
└── README.md
```

**Design Principles**:
- **One Agent Per Plugin**: Specialized tutor for each topic area
- **Multiple Skills Per Agent**: Agent invokes appropriate skills based on query
- **Cross-Agent Referrals**: Agents refer to each other when topics overlap
- **Show Workings**: Never just answers - always step-by-step calculations
- **Safety First**: Proactive warnings, color-coded results (SAFE/CAUTION/DANGER)

---

## ⚠️ Status & Roadmap

**v0.1.0 (Current)** - 2025-11-01
- ✅ 5 plugins ready for testing (17 skills total)
- ✅ Agent framework established for all 14 plugins
- ✅ Comprehensive documentation
- ✅ Chart correction skills added (5 new skills in chart-basics)
- 🚧 9 plugins with skeleton agents (skills in development)

**v0.2.0 (Planned)**
- Add positioning skills (visual fixes, EP calculator, running fix)
- Add CTS calculator with vector triangles
- Add electronic navigation skills (GPS accuracy, radar)

**v0.3.0 (Planned)**
- Add meteorology skills (synoptic charts, weather routing)
- Add IRPCS scenario tester and lights quiz
- Complete nav lights flashcard system

---

## 🤝 Contribute

We welcome contributions from the sailing community!

**Found a mistake** in calculations or theory?
**Want additional skills** for a plugin?
**Have exam questions** to add to quizzes?

Please **open an issue** or submit a **Pull Request**.

### Contributing Skills

See `claude-skills-library` for skill format and contribution guidelines:
https://github.com/ZenterFlow/claude-skills-library

**Skill Requirements**:
- Clear SKILL.md with purpose, triggers, behavior
- manifest.json with metadata
- Sample test prompts
- Resources/templates as needed

---

## 📖 Related Resources

- **Skills Library**: https://github.com/ZenterFlow/claude-skills-library (50+ sailing skills)
- **Claude Code Global**: https://github.com/ZenterFlow/claude-code-global (Setup examples)
- **RYA Syllabus**: https://www.rya.org.uk/knowledge/training-qualifications
- **ASA Syllabus**: https://asa.com/certifications/

---

## 📊 Statistics

- **Total Plugins**: 14
- **Ready for Testing**: 9 (64%)
- **Total Skills**: 68 (with more planned)
- **Total Agents**: 14
- **Lines of Documentation**: 17,000+
- **Coverage**: Full RYA/ASA YachtMaster Offshore syllabus

---

## 📝 Version History

**v0.9.0** (2025-11-10)
- Added 2 specialized positioning skills to Plugin 03
- Plugin 03 (Positioning) expanded to 8 skills: Added navigation-web-constructor (pre-plotted bearing/distance grids for rapid GPS monitoring and tacking decisions), angle-off-bow-fix (45°/90° relative bearing method for quick distance-off estimation)
- 68 total skills implemented (2 new)
- Complete specialized navigation techniques coverage
- Comprehensive duplicate check: All SKILL_15-47 reviewed, identified only 2 non-duplicate skills

**v0.8.0** (2025-11-10)
- Added 8 advanced electronic navigation and chart plotter skills
- Plugin 05 (Electronic Navigation) expanded to 16 skills: Added electronic-navigation-integration (complete system integration with paper backup), radar-overlay-verification (fog position verification), feature-radar-appearance (predict radar returns), restricted-visibility-decision (continue/stand-off decision making), ais-data-source-distinction (direct vs internet AIS)
- Plugin 06 (EC Plotting) expanded to 5 skills: Added auto-route-verification (verify auto-routes against paper charts), mobile-device-repeater (tablet/phone plotter usage), waypoint-positioning-adjustment (fog navigation waypoint offsets)
- 66 total skills implemented (8 new)
- Complete restricted visibility and fog navigation coverage
- Comprehensive electronic navigation integration

**v0.7.0** (2025-11-10)
- Added 13 electronic navigation skills across 2 plugins
- Plugin 05 (Electronic Navigation) now complete with 11 skills: GPS/GNSS fundamentals, GPS data interpretation, depth sounder configuration, radar basics, AIS target interpretation, integrated navigation, system limitations, waypoint management, instrument calibration, radar pilotage, MARPA collision assessment
- Plugin 06 (EC Plotting) now complete with 2 skills: electronic chart types (RNC vs ENC), chart plotter operation
- 58 total skills implemented (13 new)
- 9 plugins now ready for testing (64% complete)
- Complete electronic navigation and chart plotter coverage

**v0.6.0** (2025-11-10)
- Added 11 new advanced navigation skills across 3 plugins
- Plugin 02 (Tides) expanded to 8 skills: Added tidal-terminology-guide, time-zone-converter, tidal-theory-explainer
- Plugin 03 (Positioning) expanded to 6 skills: Added visual-fix-reliability, enhanced-visual-fixing, position-fix-integrator
- Plugin 04 (Course to Steer) expanded to 7 skills: Added vector-triangle-plotter, leeway-applicator, multi-factor-converter, tidal-hour-selector, cts-practical-integrator
- 45 total skills implemented (11 new)
- Complete foundational navigation and CTS workflow coverage

**v0.5.0** (2025-11-10)
- Added 4 compass error skills to Plugin 01 (Chart Basics)
- Plugin 01 now complete with 17 skills (100% RYA/ASA chart basics syllabus)
- Compass workflow: variation calculation → deviation tables → CADET conversions → hand bearing techniques
- 34 total skills implemented across 7 ready plugins
- Complete navigation fundamentals coverage

**v0.4.0** (2025-11-09)
- Added 4 new visual aids skills to Plugin 08
- Plugin 08 (Visual Aids) now complete: 5 skills (lights, cardinal marks, ranges, dipping distance)
- 7 plugins now ready for testing (50% complete)
- 30 total skills implemented
- Complete visual navigation aids coverage

**v0.3.0** (2025-11-09)
- Added 4 new pilotage skills to Plugin 09
- Plugin 09 (Pilotage) complete: 6 skills
- Safety-critical pilotage procedures complete

**v0.2.0** (2025-11-09)
- Added 5 new skills across 2 plugins
- Plugin 03 (Positioning) now ready: 3 skills (visual-fix, EP, XTE)
- Plugin 04 (Course to Steer) now ready: 2 skills (CTS calculator, velocity triangles)
- Comprehensive navigation calculation support

**v0.1.0** (2025-11-01)
- Initial marketplace release
- 5 plugins ready: Chart Basics, Tides, Passage Making, Visual Aids, Pilotage
- 17 skills implemented and tested
- 14 agent frameworks established
- Complete documentation structure

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgments

Built from real-world YachtMaster Offshore training and examination experience.

Skills consolidated from:
- **YachtMasterOffshore** project (12+ sailing/navigation skills)
- **Agentlify-Ventures** project (technical framework)
- **claude-skills-library** (50+ reusable skills)

---

**Built with** ⛵ **for sailors, by sailors**

&copy; ZenterFlow

*Last Updated: 2025-11-10*
*Version: 0.9.0 (Beta)*
