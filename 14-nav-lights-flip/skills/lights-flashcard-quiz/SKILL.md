---
name: Navigation Lights Flashcard Quiz
version: 1.0.0
triggers:
  - "quiz me on navigation lights"
  - "test my knowledge of vessel lights"
  - "lights flashcard"
  - "what lights does a"
  - "navigation lights quiz"
---

# Navigation Lights Flashcard Quiz

## Purpose
Interactive rapid-fire quiz testing recognition of navigation light configurations for all vessel types under COLREGS Rules 20-31. Essential for Yachtmaster Offshore exam preparation and practical nighttime vessel identification.

## Activation Triggers
This skill activates when users request:
- Navigation lights quizzes or flashcards
- Vessel light identification practice
- Questions about specific vessel light configurations
- Exam preparation for COLREGS lights requirements

## Behavior

### Quiz Format
Present random vessel scenarios and ask user to identify correct light configuration, or show light configuration and ask for vessel type/status. Use multiple-choice format with 4 options, including common mistakes.

### Vessel Types Covered

**Power-Driven Vessels:**
- **Under 12m**: All-round white + sidelights (or combined lantern if <7m)
- **12m-50m**: Forward masthead white, sidelights, sternlight (5nm/2nm/2nm)
- **Over 50m**: Forward masthead, aft masthead (higher), sidelights, sternlight (6nm/6nm/3nm/3nm)
- **<7m & <7kn**: All-round white only (alternative configuration)

**Sailing Vessels:**
- **Under sail alone**: Sidelights + sternlight (NO masthead light)
- **Motor-sailing**: Forward masthead + sidelights + sternlight (same as power-driven)
- **Under 7m**: Torch ready to show (practical alternative)

**Vessels at Anchor:**
- **Under 50m**: All-round white forward where best seen
- **Over 50m**: All-round white forward + all-round white aft (lower)
- **>100m**: Additional deck lights on working areas

**Vessels Aground:**
- Same as anchored + **Two all-round red lights in vertical line**

**Fishing Vessels:**
- **Trawling (underway)**: Sidelights + sternlight + green over white vertical
- **Trawling (stopped/<2kn)**: Green over white vertical only
- **Other fishing (e.g., longline)**: Sidelights + sternlight + red over white vertical
- **Gear >150m out**: White all-round light or cone in direction of gear

**Not Under Command (NUC):**
- **Making way**: Two red vertical + sidelights + sternlight
- **Not making way**: Two red vertical only

**Restricted in Ability to Maneuver (RAM):**
- **Making way**: Forward masthead, sidelights, sternlight + red-white-red vertical
- **Not making way**: Red-white-red vertical only
- **At anchor**: Anchor light + red-white-red vertical

**Constrained by Draft (CBD):**
- Same as power-driven + **Three all-round red lights in vertical line**
- **Only applies when UNDERWAY**

**Pilot Vessels:**
- **On duty, underway**: Sidelights + sternlight + white over red vertical
- **On duty, at anchor**: Anchor light + white over red vertical

**Towing & Pushing:**
- **Under 200m tow**: Forward masthead + sidelights + sternlight + yellow towing light over sternlight + diamond shape
- **Over 200m tow**: Two masthead lights forward + sidelights + sternlight + yellow towing light + diamond shape
- **Pushing ahead/alongside**: Forward masthead + sidelights + sternlight + two yellow towing lights vertical

### Light Characteristics Reference

**Arcs of Visibility:**
- Masthead light: 225° (forward-facing)
- Sidelights: 112.5° each (port red, starboard green)
- Sternlight: 135° (aft-facing)
- All-round light: 360°
- Towing light: 135° (yellow, same as sternlight)

**Visibility Ranges by Vessel Length:**
- **Under 12m**: Masthead 2nm, Sidelights 1nm, Stern 2nm
- **12m-50m**: Masthead 5nm, Sidelights 2nm, Stern 2nm
- **Over 50m**: Masthead 6nm, Sidelights 3nm, Stern 3nm

### Quiz Examples

**Example Question 1:**
*"You observe a vessel showing two white masthead lights in vertical line (aft light higher), red and green sidelights, and a white sternlight. What is this vessel?"*

A) Power-driven vessel under 50m
B) Power-driven vessel over 50m
C) Vessel towing (tow under 200m)
D) Vessel not under command making way

**Answer**: B - Power-driven vessel over 50m (aft masthead light must be higher than forward)

**Example Question 2:**
*"A sailing yacht turns on its engine while still under sail at night. What lights must it show?"*

A) Sidelights and sternlight only (no change)
B) Forward masthead light + sidelights + sternlight
C) All-round white light only
D) Tricolour light at masthead

**Answer**: B - Forward masthead light + sidelights + sternlight (motor-sailing = power-driven)

**Example Question 3:**
*"You see a vessel showing green over white vertical lights, plus sidelights and sternlight. What is this vessel doing?"*

A) Fishing with longlines
B) Trawling
C) Not under command
D) Dredging operations

**Answer**: B - Trawling (green over white = trawling, red over white = other fishing)

### Common Exam Mistakes to Test

1. **Motor-sailing**: Forgetting forward masthead light is mandatory
2. **CBD vs RAM**: Confusing three red vertical (CBD) with red-white-red (RAM)
3. **Anchor intervals**: Over 50m vessels need TWO anchor lights (forward + aft lower)
4. **Trawling colors**: Green over white (NOT red over white)
5. **Towing lights**: Yellow towing light position (over sternlight for <200m tow)
6. **NUC vs RAM**: Two red vertical (NUC) vs red-white-red vertical (RAM)
7. **Sidelight combination**: Only under 7m may combine sidelights to one lantern

### Memory Aids

- **"Green over White, Trawling at Night"** (trawling lights)
- **"Red over White, Fishing at Night"** (other fishing)
- **"White over Red, Pilot Ahead"** (pilot vessel)
- **"Three Reds High, Deep Draft Nigh"** (CBD = constrained by draft)
- **"Two Reds Bare, NUC Don't Care"** (not under command)

### Quiz Flow

1. **Start Quiz**: Ask user preference (random mix, specific vessel type, or exam simulation)
2. **Present Question**: Show light configuration or vessel scenario
3. **Accept Answer**: User selects A/B/C/D
4. **Provide Feedback**: Correct answer + explanation of why
5. **Track Score**: Keep running tally
6. **Continue**: Offer next question or summary

### Difficulty Progression

**Basic Level:**
- Simple power-driven vessels
- Basic sailing vessels
- Anchor lights

**Intermediate Level:**
- Motor-sailing configurations
- Fishing vessels (trawling vs other)
- NUC and RAM

**Advanced Level:**
- CBD distinction from RAM
- Towing over/under 200m
- Combined scenarios (e.g., RAM at anchor)
- Special cases (WIG craft, pilot vessels)

### Exam Simulation Mode

10-question rapid-fire quiz covering:
- 3 power-driven vessel questions
- 2 fishing vessel questions
- 2 special status questions (NUC/RAM/CBD)
- 1 towing question
- 1 anchor/aground question
- 1 motor-sailing/pilot question

Time limit: 1 minute per question (exam conditions)

## Version History
- **v1.0.0** (2025-11-10): Initial implementation with comprehensive COLREGS lights coverage
