---
name: hand-bearing-compass
description: Take accurate magnetic bearings of charted objects for position fixing and collision avoidance using hand-bearing compass.
license: CC-BY-SA
---

# SKILL: hand-bearing-compass
**RYA Yachtmaster – Hand Bearing Compass Techniques**

## Purpose
Teach proper use of hand-bearing compass for taking accurate magnetic bearings of charted objects, position fixing through cross bearings, and collision avoidance using steady bearing analysis.

## Activation Triggers
- "Hand bearing compass"
- "Take a bearing"
- "Cross bearings"
- "Position fix"
- "Steady bearing"
- "Collision avoidance bearing"
- "Three point fix"

## Behaviour
1. Identify the user's intent:
   - **Position fixing**: Using multiple bearings to determine vessel position
   - **Collision avoidance**: Monitoring approaching vessel bearings
   - **General technique**: How to take accurate bearings

2. For position fixing:
   - Guide selection of 2-3 conspicuous charted objects
   - Explain ideal bearing spread (45-90° between objects)
   - Teach sequential bearing technique (complete within 2 minutes)
   - Show plotting method: from objects seaward
   - Explain cocked hat interpretation

3. For collision avoidance:
   - Teach steady bearing = collision risk principle
   - Explain multiple bearing technique over time
   - Show how to interpret bearing changes
   - Emphasize action required for steady bearings

4. Emphasize deviation minimization:
   - Stand away from metal objects (engine, speakers, tools, rigging)
   - Keep compass level and steady at eye height
   - Use at arm's length from body
   - **CRITICAL**: No deviation table applies to hand-bearing compass
   - Bearings are always magnetic (need variation for true)

5. Common errors to address:
   - Taking bearings too close to metal structure
   - Too much time between sequential bearings
   - Poor object selection (low, indistinct features)
   - Forgetting variation correction
   - Expecting steering compass accuracy

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor prompt with techniques
- `templates/position-fix-procedure.md` – step-by-step position fixing
- `templates/collision-avoidance-guide.md` – steady bearing technique
- `templates/bearing-worksheet.md` – practice recording format
- `tests/sample-prompts.md` – validation questions
- `resources/deviation-sources.md` – magnetic interference guide
- `resources/object-selection-guide.md` – choosing good targets

## Example Session

**User:** "How do I take a position fix using hand bearing compass?"

**Skill:**
```
HAND BEARING COMPASS POSITION FIX

1. SELECT OBJECTS
   Choose 2-3 conspicuous charted features:
   ✓ Lighthouses, church spires, headlands
   ✓ 45-90° bearing spread between objects
   ✓ Visible and positively identified
   ✗ Avoid: low features, similar objects

2. MINIMIZE DEVIATION
   - Stand away from metal (minimum 2m from engine)
   - Remove metal objects from pockets
   - Keep compass level at eye height
   - Hold steady during sighting

3. TAKE BEARINGS (quickly, <2 minutes total)
   Example readings:
   - Church spire: 045°(M)
   - Lighthouse: 120°(M)
   - Headland: 280°(M)

4. PLOT ON CHART
   - Find each object on chart
   - Apply reverse bearing (add/subtract 180°)
   - Draw position line FROM object SEAWARD
   - Intersection = vessel position

5. ASSESS ACCURACY
   - Small cocked hat: good fix
   - Large cocked hat: retake bearings or check object ID
   - Assume position at danger side of cocked hat

⚠️ REMEMBER: These are MAGNETIC bearings
   - Add variation correction for True bearings
   - No deviation table applies (hand-bearing compass)
```

**User:** "Vessel approaching, how do I check collision risk?"

**Skill:**
```
COLLISION AVOIDANCE: STEADY BEARING CHECK

Principle: If bearing remains constant → collision risk exists

TECHNIQUE:
1. Take initial bearing of approaching vessel
   Example: 315°(M) at 10:00

2. Wait 3-5 minutes (or appropriate interval)

3. Take second bearing
   Example: 315°(M) at 10:04

4. INTERPRET RESULTS:

   📍 Bearing STEADY (315° → 315°)
      → COLLISION RISK
      → Take avoiding action (alter course/speed)

   📍 Bearing DRAWING AFT (315° → 320°)
      → Vessel passing astern
      → Monitor but lower risk

   📍 Bearing DRAWING FORWARD (315° → 310°)
      → Vessel passing ahead
      → Monitor but lower risk

⚠️ SAFETY RULES:
- Take multiple bearings to confirm trend
- Act early if bearing steady
- Remember COLREGS right-of-way rules
- Don't rely on single bearing
- In doubt: assume collision risk and act

💡 TIP: Mark bearing on chart to visualize CPA
```

## Key Concepts
- **Cross bearings**: 2-3 bearings create position fix where lines intersect
- **Steady bearing = collision risk**: Fundamental collision avoidance principle
- **No deviation table**: Hand-bearing compass cannot be corrected like ship's compass
- **Magnetic bearings only**: Always apply variation for true bearings
- **Quick sequential bearings**: Complete within 2 minutes to minimize position drift
- **Proper technique**: Distance from metal, level compass, steady hold
- **Cocked hat**: Triangle formed by three position lines (smaller = more accurate)
