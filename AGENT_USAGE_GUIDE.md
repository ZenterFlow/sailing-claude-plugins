# Sailing Navigation Agent - Usage Guide

## Overview

This repository includes **conversational AI agents** that serve as your personal sailing tutor and navigation companion. The agents can adapt to different modes based on your needs.

## Quick Start

### Activate the Agent

```bash
# In Claude Code or compatible AI assistant:
/sailing-mode
```

Or just start talking about sailing:
```
"I need help with tidal calculations"
"What's the difference between DR and EP?"
"Should I tack now?" (while sailing)
```

The agent will automatically detect your needs and switch to the appropriate mode.

## Operating Modes

### 🎓 Learning Mode (Shore-Based Study)

**When to use**: Studying at home, preparing for exams, deep learning

**Features**:
- Interactive lessons with visual descriptions
- Step-by-step worked examples
- Quizzes and progress tracking
- Detailed concept explanations
- Practice problems with feedback

**Example conversations**:
```
You: "Teach me about tidal curves"
Agent: [Provides structured lesson with visuals and practice]

You: "Quiz me on chart symbols"
Agent: [Runs interactive 10-question quiz with feedback]

You: "I don't understand velocity triangles"
Agent: [Explains concept with diagrams and examples]
```

### ⛵ Active Sailing Mode (Real-Time On-Water)

**When to use**: While actively sailing, need immediate answers

**Features**:
- Voice-optimized short responses
- Quick calculations (CTS, ETA, position)
- Safety warnings and hazard checks
- Tactical sailing advice
- Immediate decision support

**Example conversations**:
```
You: "What's my ETA to Portsmouth at 6 knots?"
Agent: "34 miles divided by 6 knots = 5.7 hours. ETA 17:42."

You: "Should I reef now?"
Agent: "What's your wind speed? Above 20 knots true, reef now.
Below 20, you're fine with full main."

You: "Depth check - reading 4.2m, tide is HW-2"
Agent: "Tide is +1.8m. Actual charted depth is 2.4m.
With 1.8m draught you have 0.6m clearance. That's TIGHT!"
```

### 📋 Passage Planning Mode (Pre-Departure)

**When to use**: Planning a passage, route optimization

**Features**:
- Step-by-step passage planning
- Waypoint calculation
- Tidal window analysis
- Hazard identification
- Weather routing

**Example conversation**:
```
You: "Plan passage from Cowes to Cherbourg"
Agent: "Great passage! Let's plan it:

1. Distance: 58nm
2. Best departure: HW Dover -2 for favorable stream
3. Waypoints needed: 3 (Needles, mid-Channel, Cherbourg approach)
4. Hazards: Alderney Race, commercial traffic in TSS
5. Estimated passage time: 10-12 hours at 5-6 knots

Want me to calculate specific waypoints?"
```

## Available Topics (68 Skills Across 14 Domains)

### Core Navigation
1. **Chart Basics** (17 skills) - Datums, symbols, corrections, compass
2. **Tides** (8 skills) - Heights, streams, calculations
3. **Positioning** (8 skills) - Fixes, DR, EP, XTE, navigation webs
4. **Course to Steer** (7 skills) - CTS, velocity triangles, leeway

### Modern Navigation
5. **Electronic Navigation** (16 skills) - GPS, radar, AIS, fog navigation
6. **EC Plotting** (5 skills) - Chart plotters, auto-routes, waypoints

### Practical Skills
7. **Passage Making** (1 skill) - Almanac, port planning
8. **Visual Aids** (5 skills) - Buoyage, lights, marks
9. **Pilotage** (6 skills) - Harbor entry, clearing bearings

### Advanced (Coming Soon)
10. **Meteorology** - Weather, forecasts
11. **IRPCS** - Collision regulations
12. **Safety & Environment** - Emergency procedures
13. **Collision Regs** - Rules of the road
14. **Nav Lights** - Recognition quiz

## How the Agent Adapts

The agent automatically detects what you need:

**Learning Indicators**:
- "Explain...", "Teach me...", "How does... work?"
- "Quiz me on..."
- "I don't understand..."
→ **Switches to Learning Mode**: Detailed teaching

**Active Sailing Indicators**:
- "Quick -...", "What's my...", "Should I...?"
- Time-sensitive language
- Single direct questions
→ **Switches to Active Mode**: Fast, concise answers

**Planning Indicators**:
- "Plan passage to..."
- "Route from... to..."
- "When should I leave?"
→ **Switches to Planning Mode**: Systematic planning

## Example Full Sessions

### Learning Session

```
You: Start learning session

Agent: 👋 Welcome to your Sailing YachtMaster Tutor!

What would you like to work on today?
• Learn a new topic
• Practice with quizzes
• Review weak areas
• Exam prep guidance

You: Quiz me on tides

Agent: 📝 Tidal Heights Quiz (5 questions)

Question 1/5:
HW Portsmouth: 11:25 UTC at 4.7m
LW Portsmouth: 17:50 UTC at 1.2m
What's the height at 14:30?

A) 2.5m
B) 2.9m
C) 3.2m
D) 3.8m

[Interactive quiz continues with detailed feedback]
```

### Active Sailing Session

```
You: Position check

Agent: What's your GPS position or last known fix?

You: 50°42.3'N 001°18.5'W

Agent: ✓ Checked:
• 3.2nm SW of Needles
• Clear of hazards
• Depth ~15m at this location
• TSS 8nm south - monitor traffic

Destination?

You: Poole Harbor entrance

Agent: 📍 Poole: 12.4nm @ 045°T
⏱️ ETA at 5 knots: 2.5 hours = 16:12
🌊 Tidal gate: Need HW-2 to HW+2 for entry
Current time 13:42, HW 15:30 → Window 13:30-17:30
✓ You'll arrive in the window. Good timing!

Want course to steer with tidal stream?
```

## Tips for Best Experience

### For Learning
- Be specific about what you want to learn
- Request quizzes to test knowledge
- Ask follow-up questions freely
- Request visual descriptions

### For Active Sailing
- Keep questions short and direct
- Provide essential context (position, conditions)
- Use voice input if possible
- Ask for options when making decisions

### For Planning
- Provide departure and destination clearly
- Mention any timing constraints
- Ask about specific concerns (tides, hazards)
- Request waypoint coordinates if needed

## Switching Modes

You can explicitly switch modes:

```
"Switch to learning mode"
"Switch to active sailing mode"
"Switch to planning mode"
```

Or the agent will adapt automatically based on your questions.

## Advanced Features

### Progress Tracking (Learning Mode)
The agent can remember within a session:
- Topics you've covered
- Quiz performance
- Difficult concepts
- Suggested next topics

### Context Awareness (Active Mode)
The agent tracks:
- Current position (if provided)
- Destination waypoints
- Vessel characteristics
- Tidal state
- Weather conditions

### Multi-Option Decision Support
When asking "should I?", the agent provides:
1. Recommended option
2. Conservative option
3. Aggressive option
4. Trade-offs for each

## Safety Notice

⚠️ **Important**: This agent is a learning and decision-support tool. It should:
- ✓ Supplement your navigation skills
- ✓ Help you learn and understand concepts
- ✓ Provide calculations and checks
- ✓ Suggest options for decisions

It should NOT:
- ✗ Replace proper navigation training
- ✗ Substitute for paper charts and official publications
- ✗ Override your judgment as skipper
- ✗ Be the sole basis for safety-critical decisions

**You are the skipper - final decisions are always yours!**

## Getting Help

Within any mode, you can ask:
- "How do I use this agent?"
- "What can you help me with?"
- "Switch to [mode] mode"
- "Explain [topic]"

The agent is designed to be helpful, adaptive, and conversational. Just talk naturally about sailing and navigation!

---

**Ready to start?** Just ask a sailing question or type `/sailing-mode` to begin! 🧭⛵

