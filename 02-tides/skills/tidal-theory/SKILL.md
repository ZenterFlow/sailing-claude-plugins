---
name: tidal-theory
description: Understand astronomical causes of tides, spring/neap cycles, and tidal patterns (diurnal, semidiurnal, mixed) for passage planning and exam prep.
license: CC-BY-SA
---

# SKILL: tidal-theory
**RYA Yachtmaster – Tidal Theory and Cycle Patterns**

## Purpose
Explain the astronomical causes of tides, distinguish between spring and neap tides, identify tidal patterns (diurnal, semidiurnal, mixed), and understand how lunar cycles affect tide timing for passage planning and exam preparation.

## Activation Triggers
- "explain tides"
- "spring vs neap tides"
- "why do tides happen"
- "tidal patterns"
- "diurnal vs semidiurnal"
- "lunar influence on tides"
- "why tides vary by location"
- "24 hour 50 minutes"

## Behaviour
1. **Educational Mode**: Provide clear explanations with diagrams
   - Use visual ASCII diagrams from templates
   - Explain gravitational forces (Moon, Sun, Earth)
   - Show spring/neap cycle timing relative to moon phases
   - Illustrate three tidal patterns with examples

2. **Interactive Teaching**:
   - Ask what aspect of tides the user wants to understand
   - Offer worked examples from real locations
   - Test understanding with quiz questions
   - Correct common misconceptions

3. **Common Topics**:
   - **Tidal Causes**: Moon's gravity, Sun's gravity, centrifugal force
   - **Spring Tides**: Occur 1-2 days after new/full moon (syzygy)
   - **Neap Tides**: Occur 1-2 days after quarter moons (quadrature)
   - **Lunar Day**: 24h 50min causes ~50min daily delay in tide times
   - **Patterns**: Semidiurnal (2 equal HW/LW), Diurnal (1 HW/LW), Mixed (2 unequal HW/LW)

4. **Use Templates**:
   - `templates/spring-neap-cycle.md` for moon phase diagrams
   - `templates/tidal-patterns.md` for pattern comparisons
   - `templates/gravitational-forces.md` for force explanations

5. **Exam Preparation**:
   - Emphasize timing lag (1-2 days after moon phases)
   - Explain why opposite side of Earth has tides
   - Highlight location-specific patterns

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor-level briefing
- `templates/` – educational diagrams and explanations
- `resources/` – reference materials and further reading
- `tests/sample-prompts.md` – 7 test questions

## Example Session
**User**: "Why do we get spring tides?"
**Skill**: "Spring tides occur when the Sun and Moon are aligned (at new moon or full moon), combining their gravitational pulls. This happens approximately every 14 days. The tides themselves appear 1-2 days AFTER the moon phase due to the inertia of water masses. Spring tides have the largest range between high and low water.

[Shows diagram from templates/spring-neap-cycle.md]

Would you like me to explain neap tides or show you how to predict spring tide dates for passage planning?"
