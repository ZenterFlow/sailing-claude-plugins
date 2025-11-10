# Plugin 00: Navigation Master Coordinator

**Status**: ✅ Complete - Master routing and orchestration system

**Purpose**: Intelligent coordinator that routes questions to appropriate specialized agents and orchestrates multi-plugin workflows for comprehensive navigation education.

---

## 🎯 What This Does

The Navigation Master Coordinator is your **unified interface** to all 14 sailing navigation plugins. Instead of knowing which plugin handles which topic, you simply ask your navigation questions and the master coordinator:

1. **Analyzes** your question to identify required knowledge domains
2. **Routes** to the appropriate specialized agent(s) automatically
3. **Orchestrates** responses from multiple plugins when needed
4. **Synthesizes** comprehensive answers from multiple domains

---

## 🚀 Quick Start

### Simple Questions (Single Plugin)
Ask naturally - the coordinator routes automatically:

```
User: "What datum is BA 2454?"
→ Routes to Plugin 01 (Chart Basics)

User: "Calculate tide height at 1430"
→ Routes to Plugin 02 (Tides)

User: "What lights does a trawler show?"
→ Routes to Plugin 11 (IRPCS)
```

### Complex Questions (Multiple Plugins)
The coordinator orchestrates multi-domain workflows:

```
User: "Plan passage Southampton to Cherbourg with weather routing"

Coordinator orchestrates:
1. Plugin 07: Overall passage plan and almanac info
2. Plugin 02: Tidal calculations for route
3. Plugin 04: Course to steer with tidal effects
4. Plugin 10: Weather window analysis
5. Plugin 09: Cherbourg harbor entry plan

→ Delivers integrated response combining all domains
```

---

## 🧭 Available Specialists (14 Plugins)

The coordinator has access to these specialized tutors:

### Navigation Fundamentals
- **Plugin 01**: Chart Basics (17 skills) - Charts, symbols, datums, compass
- **Plugin 02**: Tides (8 skills) - Tidal calculations and streams
- **Plugin 03**: Positioning (8 skills) - Visual fixes, EP, DR
- **Plugin 04**: Course to Steer (7 skills) - CTS with tide and leeway

### Electronic Systems
- **Plugin 05**: Electronic Navigation (16 skills) - GPS, radar, AIS
- **Plugin 06**: EC Plotting (5 skills) - Chart plotters and waypoints

### Passage & Pilotage
- **Plugin 07**: Passage Making (5 skills) - Planning, prep, safety brief
- **Plugin 09**: Pilotage (13 skills) - Harbor entry, clearing bearings

### Visual Navigation
- **Plugin 08**: Visual Aids (11 skills) - Buoys, lights, marks

### Weather
- **Plugin 10**: Meteorology (6 skills) - Forecasts, systems, clouds

### Collision Regulations
- **Plugin 11**: IRPCS (7 skills) - Complete COLREGS Rules 1-37
- **Plugin 14**: Nav Lights Flip (3 skills) - Lights/shapes/signals quizzes

### Safety & Emergency
- **Plugin 12**: Safety & Environment (7 skills) - Emergency procedures

---

## 💡 Usage Examples

### Example 1: Single-Domain Question
```
User: "How do I calculate under-keel clearance?"

Master: [Identified Domain: Plugin 02 - Tides]

Routing to Tides Tutor...

Tides Tutor: Under-Keel Clearance (UKC) Calculation:

Formula: UKC = (Charted Depth + Height of Tide) - (Draught + Safety Margin)

[Complete tidal calculation response...]
```

### Example 2: Multi-Domain Orchestration
```
User: "Approaching harbor in fog, what do I do?"

Master: [Complex Question - Multiple Domains Required]

Domains involved:
• Plugin 12: Safety (fog procedures)
• Plugin 11: IRPCS (fog signals, safe speed)
• Plugin 09: Pilotage (depth contour navigation)
• Plugin 05: Electronic Nav (radar operation)

Coordinated Response:

**Step 1: Immediate Actions (Safety)**
First 2 minutes checklist:
1. Establish position (GPS)
2. Don life jackets (all crew)
3. Deploy radar reflector
[...]

**Step 2: Regulatory Compliance (IRPCS)**
Sound signals: One prolonged + two short (sailing vessel)
Safe speed: Stop within half visible distance
[...]

**Step 3: Navigation Strategy (Pilotage)**
Primary method: Depth contour following
10% circle of error for buoy positions
[...]

**Step 4: Electronic Aids (Electronic Nav)**
Radar: Target acquisition, CPA/TCPA assessment
GPS: Secondary confirmation only
[...]

**Integrated Solution:**
[Comprehensive fog approach procedure synthesizing all domains]
```

### Example 3: Exam Preparation
```
User: "Help me prepare for YachtMaster Offshore exam"

Master: YachtMaster Offshore Exam Preparation Plan

I'll guide you through the complete syllabus across 13 plugins:

**Phase 1: Navigation Fundamentals (Plugins 01-04)**
Week 1: Chart Basics - datums, symbols, compass errors
Week 2: Tides - height/stream calculations
Week 3: Positioning - visual fixes, EP, DR
Week 4: Course to Steer - tide and leeway

**Phase 2: Electronic & Visual (Plugins 05-06, 08)**
[...]

**Phase 3: Practical Planning (Plugins 07, 09-10)**
[...]

**Phase 4: Rules & Safety (Plugins 11-12)**
[...]

**Phase 5: Quiz & Practice (Plugin 14)**
[...]

Ready to start with Phase 1? [Y/N]
```

---

## 🔄 Common Workflows

### Pre-Departure Workflow
*Trigger*: "I'm departing tomorrow, what do I need to check?"

**Orchestration**:
1. **Plugin 07**: Pre-departure safety briefing checklist
2. **Plugin 02**: Calculate tidal information for departure
3. **Plugin 10**: Review weather forecast
4. **Plugin 01**: Verify charts are current
5. **Plugin 07**: Establish shore contact with "latest arrival"

### Harbor Entry Workflow
*Trigger*: "Entering [Harbor] at night"

**Orchestration**:
1. **Plugin 07**: Almanac info (VHF, HW times, pilotage notes)
2. **Plugin 09**: Pilotage plan (leading lines, clearing bearings)
3. **Plugin 08**: Navigation lights and marks identification
4. **Plugin 02**: Tidal height for entry
5. **Plugin 11**: Maneuvering signals and rules

### Complete Navigation Problem
*Trigger*: "Plot course from A to B accounting for tide and leeway"

**Orchestration**:
1. **Plugin 01**: Compass corrections, chart symbols
2. **Plugin 03**: Plot current position
3. **Plugin 02**: Calculate tidal stream component
4. **Plugin 04**: Calculate course to steer with tide and leeway

---

## 🎓 Learning Path Recommendations

### Beginner Path
1. Start with **Plugin 01** (Chart Basics) - Foundation
2. Progress to **Plugin 02** (Tides) - Essential calculations
3. Learn **Plugin 03** (Positioning) - Fix your position
4. Master **Plugin 04** (Course to Steer) - Navigate accurately

### Intermediate Path
5. **Plugin 08** (Visual Aids) - Identify marks and lights
6. **Plugin 09** (Pilotage) - Harbor approaches
7. **Plugin 07** (Passage Making) - Plan passages
8. **Plugin 10** (Meteorology) - Weather analysis

### Advanced Path
9. **Plugin 05-06** (Electronic Navigation) - Modern systems
10. **Plugin 11** (IRPCS) - Collision regulations
11. **Plugin 12** (Safety) - Emergency procedures

### Exam Prep
12. **Plugin 14** (Nav Lights Flip) - Rapid-fire quizzes

---

## 🧠 Intelligent Routing Features

### Ambiguity Resolution
If question is ambiguous, the coordinator asks for clarification:

```
User: "How do I calculate range?"

Master: "Range" could refer to multiple topics:
A) Dipping distance of navigation lights (Plugin 08)
B) Radar range calculations (Plugin 05)
C) Fuel range/consumption (Plugin 07)

Which would you like help with? [A/B/C]
```

### Context Awareness
The coordinator remembers conversation context:

```
User: "What's the tide height at 1430?"
Master: [Routes to Plugin 02, provides answer]

User: "And what about UKC?"
Master: [Understands context, continues with Plugin 02 for UKC calculation]
```

### Cross-Plugin Skill Sharing
Some skills appear in multiple plugins - coordinator routes to best fit:

- **almanac-navigator**: Plugin 07 (planning) OR Plugin 09 (pilotage entry)
- **restricted-visibility**: Plugin 09 (pilotage) OR Plugin 12 (safety) OR Plugin 05 (radar)

Routing decision based on user's context and intent.

---

## 📊 Coverage Statistics

**Total Specialists**: 13 complete plugins
**Total Skills**: 108 navigation skills
**YachtMaster Syllabus**: 100% theory coverage
**Domains Covered**: 7 major navigation domains

---

## 🎯 Design Philosophy

### Seamless Integration
Users don't need to know:
- Which plugin handles which topic
- How to invoke specific agents
- Plugin boundaries or overlaps

Just ask navigation questions naturally - the coordinator handles routing.

### Comprehensive Synthesis
Real-world navigation problems span multiple domains. The coordinator:
- Identifies all required knowledge areas
- Orchestrates responses from multiple specialists
- Synthesizes integrated solutions
- Ensures nothing is missed

### Exam-Ready Structure
Organized to match YachtMaster Offshore syllabus:
- All 7 exam sections covered
- Logical progression through topics
- Quiz-based practice available
- Complete theory preparation

---

## 🚢 Real-World Scenario Handling

### Scenario: Night Passage in Busy Shipping Lane
*Question*: "Night passage through TSS - what do I need to know?"

**Coordinator orchestrates**:
1. **Plugin 11**: TSS navigation rules, vessel hierarchy
2. **Plugin 14**: Identify vessel types from navigation lights
3. **Plugin 08**: TSS buoyage and marks
4. **Plugin 05**: AIS target interpretation, CPA/TCPA
5. **Plugin 03**: Cross-track error monitoring

→ Comprehensive night passage guidance

### Scenario: Emergency in Heavy Weather
*Question*: "Engine failure in F8 conditions, 20nm offshore"

**Coordinator orchestrates**:
1. **Plugin 12**: Deploy drogue/sea anchor procedures
2. **Plugin 12**: EPIRB activation and Mayday protocols
3. **Plugin 11**: NUC signals and obligations
4. **Plugin 10**: Weather assessment and tactics
5. **Plugin 07**: Emergency contingency planning

→ Complete emergency response protocol

---

## 🔧 Technical Details

### Routing Algorithm
1. **Question Analysis**: Parse user intent and domain keywords
2. **Domain Matching**: Map to plugin specializations
3. **Complexity Assessment**: Single vs multi-domain
4. **Orchestration**: Sequence specialist responses
5. **Synthesis**: Integrate into coherent answer

### Plugin Registry
Coordinator maintains complete registry of:
- 14 plugin identities and capabilities
- 108 skill specifications
- Cross-plugin skill mappings
- Domain overlap handling

### Workflow Engine
Manages complex multi-plugin workflows:
- Sequential orchestration (step-by-step)
- Parallel data gathering (efficiency)
- Context preservation (memory)
- Response synthesis (integration)

---

## Version History

- **v1.0.0** (2025-11-10): Initial master coordinator implementation

---

## Agent

See `agents/navigation-master.md` for complete master coordinator agent specification with routing rules, orchestration patterns, and workflow definitions.

---

**The Navigation Master Coordinator is your single point of entry to the complete sailing curriculum. Ask anything - it knows where to route your question.**
