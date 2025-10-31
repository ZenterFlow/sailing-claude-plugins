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
/plugin install passage-making@sailing-curriculum
/plugin install visual-aids@sailing-curriculum
/plugin install pilotage@sailing-curriculum

# In development (skeleton agents, no skills yet)
/plugin install positioning@sailing-curriculum
/plugin install course-to-steer@sailing-curriculum
# ... and 7 more
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

### ✅ Ready for Testing (5 plugins, 11 skills)

| Plugin | Agent | Skills | Status |
|--------|-------|--------|--------|
| **01. Chart Basics** | Chart Basics Tutor | 4 skills: datum-guardian, charted-height-interpreter, symbol-spotter, compass-converter | ✅ Ready |
| **02. Tides** | Tides Tutor | 5 skills: tide-calculator, tidal-diamond-reader, diamond-dispatcher, depth-datum-flipper, vertical-clearance-solver | ✅ Ready |
| **07. Passage Making** | Passage Making Tutor | 1 skill: almanac-navigator | ✅ Ready |
| **08. Visual Aids** | Visual Aids Tutor | 1 skill: direction-of-buoyage-reminder | ✅ Ready |
| **09. Pilotage** | Pilotage Tutor | 2 skills: chart-update-checker, almanac-navigator | ✅ Ready |

### 🚧 In Development (9 plugins)

| Plugin | Agent | Topics Covered |
|--------|-------|----------------|
| **03. Positioning** | Positioning Tutor | EP, DR, visual fixes, leeway, cross-track error |
| **04. Course to Steer** | Course to Steer Tutor | CTS calculations, leeway, tidal stream vectors |
| **05. Electronic Nav** | Electronic Nav Tutor | GPS/GNSS, radar, AIS, instruments |
| **06. EC Plotting** | EC Plotting Tutor | Chart plotter operation, ENC/RNC, validation |
| **10. Meteorology** | Meteorology Tutor | Forecasts, clouds, pressure systems, sea state |
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
**Topics**: Chart datum, symbols, Mercator projection, compass errors
**Skills**:
- datum-guardian (GPS ↔ chart datum shifts)
- charted-height-interpreter (HAT, MHWS, CD, LAT datums)
- symbol-spotter (100+ chart symbols quiz)
- compass-converter (True ↔ Magnetic ↔ Compass)

**Triggers**: "datum shift", "chart symbol", "variation and deviation", "WGS-84 vs ED-50"

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

**v0.1.0 (Current)** - 2025-10-31
- ✅ 5 plugins ready for testing (11 skills total)
- ✅ Agent framework established for all 14 plugins
- ✅ Comprehensive documentation
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
- **Ready for Testing**: 5 (36%)
- **Total Skills**: 11 (with 20+ more planned)
- **Total Agents**: 14
- **Lines of Documentation**: 5,000+
- **Coverage**: Full RYA/ASA YachtMaster Offshore syllabus

---

## 📝 Version History

**v0.1.0** (2025-10-31)
- Initial marketplace release
- 5 plugins ready: Chart Basics, Tides, Passage Making, Visual Aids, Pilotage
- 11 skills implemented and tested
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

*Last Updated: 2025-10-31*
*Version: 0.1.0 (Early Beta)*
