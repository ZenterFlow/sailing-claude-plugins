# Getting Started with Sailing Navigation Agents

## What Are These Agents?

This repository now includes **conversational AI agents** that transform the 68 sailing skills into an interactive learning and navigation system. Think of it as having an expert sailing instructor and navigator available 24/7.

## Three Modes in One System

### 🎓 Learning Mode - Your Personal Sailing Tutor
**Perfect for**: Study sessions at home, exam prep, understanding concepts

Talk to the agent like a tutor:
- "Teach me about tidal curves"
- "Quiz me on chart symbols"
- "I don't understand velocity triangles"
- "Help me prepare for my YachtMaster exam"

**Features**:
- Visual descriptions of diagrams and charts
- Step-by-step worked examples
- Interactive quizzes with instant feedback
- Progress tracking within sessions
- Detailed concept explanations

### ⛵ Active Sailing Mode - Your On-Water Companion
**Perfect for**: Real-time assistance while sailing

Quick, voice-friendly responses to immediate questions:
- "What's my ETA at 6 knots?"
- "Should I reef now?"
- "Can I clear that headland?"
- "Quick position check"

**Features**:
- Short, actionable responses (1-2 sentences)
- Fast calculations (CTS, ETA, tides)
- Safety warnings
- Tactical decision support
- Multiple option suggestions

### 📋 Planning Mode - Pre-Departure Assistant
**Perfect for**: Passage planning before you leave

Systematic route planning:
- "Plan passage from Cowes to Cherbourg"
- "What's the best departure time for Portsmouth?"
- "Identify hazards on route to Alderney"

**Features**:
- Waypoint calculations
- Tidal window analysis
- Weather routing
- Hazard identification
- Step-by-step planning workflow

## Quick Start

### Option 1: Use the Mode Selector

```
/sailing-mode
```

The agent will ask which mode you need and activate it.

### Option 2: Just Start Talking

The agent automatically detects your needs:

```
"Explain how tides work" → Learning Mode
"What's 15nm at 5 knots?" → Active Mode
"Plan route to Poole" → Planning Mode
```

## Example Conversations

### Learning Mode Example

```
You: "I need to learn about course to steer calculations"

Agent: "Great! Course to Steer (CTS) is one of the most important
navigation calculations. Let me break it down:

CTS accounts for:
1. Magnetic variation (chart → compass)
2. Deviation (compass error)
3. Tidal stream (set and drift)
4. Leeway (wind effect)

Have you worked with velocity triangles before? This will help
me know where to start."

You: "Not really"

Agent: "Perfect, let's start from the beginning. Imagine you want
to go from point A to point B...

[Continues with visual description and examples]

Ready to try a practice problem?"
```

### Active Sailing Mode Example

```
You: "I'm approaching the Needles, wind is 18 knots SW, should I reef?"

Agent: "18 knots SW - reef now if you're uncomfortable.

Wind will accelerate around the Needles - could hit 22-25 knots.

Better to reef in calm water now than struggle in the overfalls.

One reef in main, keep full genoa."

You: "What's my course through the Needles channel?"

Agent: "Needles channel: 065°T inbound, 245°T outbound.

Which way are you heading?"

You: "Outbound"

Agent: "Steer 245°T. Watch for:
- North Head on starboard
- Bridge on port
- Strong tidal stream (up to 4 knots at springs)
- Commercial traffic - stay starboard side

Current tide state?"
```

### Planning Mode Example

```
You: "Plan passage from Hamble to Cherbourg"

Agent: "📋 Hamble to Cherbourg Passage Plan

DISTANCE: 68nm
EST. TIME: 11-14 hours (at 5-6 knots)

WAYPOINTS NEEDED:
1. Hamble Point departure
2. East Bramble buoy
3. Nab Tower
4. Mid-Channel (50°10'N 001°30'W)
5. Cherbourg approach

TIDAL CONSIDERATIONS:
- Leave Hamble: HW Southampton -1 to +1
- Cross to France: HW Dover +2 for fair stream
- Best window: Depart 05:00 BST, arrive 16:00 BST

HAZARDS:
- Bramble Bank (covers at HW)
- Commercial shipping in Solent
- TSS off Cherbourg (monitor VHF 13)
- Cherbourg breakwater - enter via E entrance

Want me to calculate specific waypoint coordinates?"
```

## How to Get the Most Out of the Agents

### For Learning Sessions
1. **Be specific** about what you want to learn
2. **Ask for quizzes** to test your knowledge
3. **Request visual descriptions** for diagrams
4. **Follow up** with questions if something's unclear
5. **Practice problems** - the more you do, the better you learn

### For Active Sailing
1. **Keep questions short** - the agent knows to be concise
2. **Provide context** - position, conditions, vessel details
3. **Use voice** input if possible (hands-free)
4. **Ask for options** when making tactical decisions
5. **Safety first** - the agent will prioritize hazard warnings

### For Passage Planning
1. **State your route** clearly (from X to Y)
2. **Mention constraints** (departure time, weather windows)
3. **Ask about specifics** (tides, hazards, waypoints)
4. **Request calculations** for distances, bearings, ETAs
5. **Verify** - always double-check with charts and pilots

## What the Agent Knows

The agent has deep knowledge of 68 navigation skills:

**Core Topics** (Complete):
- Chart Basics: 17 skills
- Tides: 8 skills
- Positioning: 8 skills
- Course to Steer: 7 skills
- Electronic Navigation: 16 skills
- EC Plotting: 5 skills
- Visual Aids: 5 skills
- Pilotage: 6 skills

**Coming Soon**:
- Meteorology
- IRPCS (Collision Regulations)
- Safety & Environment
- Nav Lights Recognition

## Safety & Limitations

### ✅ The Agent IS Good For:
- Learning navigation concepts
- Practicing calculations
- Decision support and options
- Quick reference while sailing
- Exam preparation

### ⚠️ The Agent is NOT a Substitute For:
- Proper navigation training
- Official charts and publications
- Your judgment as skipper
- Professional weather forecasts
- Emergency services

**Always remember**: You are the skipper. The agent provides information and suggestions, but **final decisions are yours**.

## Switching Between Modes

You can explicitly switch:
```
"Switch to learning mode"
"Switch to active sailing mode"
"Switch to planning mode"
```

Or let the agent detect automatically based on your questions.

## Tips & Tricks

### Voice Usage (Active Mode)
- Speak naturally - the agent handles filler words
- Say numbers clearly: "one-five" for 15
- The agent will repeat critical info
- Confirm understanding: "Did you get that?"

### Learning Efficiency
- Start sessions with clear goals
- Take quizzes to identify weak areas
- Review concepts you got wrong
- Practice problems build muscle memory

### Planning Workflow
- Plan the night before departure
- Review tides for entire passage
- Identify contingency harbors
- Note VHF channels for route

## Getting Help

Ask the agent at any time:
```
"How do I use you?"
"What can you help me with?"
"Switch to [mode name] mode"
"Explain [any sailing topic]"
```

The agent is conversational - just talk naturally about sailing!

## What's Next?

This is version 1.0 of the agent system. Future enhancements:
- Persistent user profiles and progress tracking
- Visual diagram generation
- Integration with chart plotting software
- Weather data integration
- Exam simulation mode

---

**Ready to start?**

Just say: "Let's learn about navigation" or "Help me with sailing"

The agent will take it from there! 🧭⛵

