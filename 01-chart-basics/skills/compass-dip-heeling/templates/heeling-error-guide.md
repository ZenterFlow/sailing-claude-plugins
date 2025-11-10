# Heeling Error: Practical Recognition and Mitigation

## What Is Heeling Error?

**Definition:**
Compass deviation caused by vessel heel angle, creating false horizontal magnetic force from Earth's vertical dip component.

**Key Characteristic:**
Unlike standard deviation, heeling error:
- Changes with every change in heel angle
- Varies with heading
- Cannot be tabulated like deviation
- Cannot be corrected by compass adjustment

## The Physical Mechanism

### Vessel Upright (No Heeling Error)
```
        ↑ Vertical (gravity)
        │
        │  ┌──────────────┐
        │  │   COMPASS    │
        │  │  ┌────────┐  │
        │  │  │ N ═══ E│  │  Horizontal forces only
        │  │  │        │  │  measured by compass
        │  │  └────────┘  │
        │  └──────────────┘
        │
═══════════════════════════ Deck (level)

Vertical dip force: Acts through pivot (no effect on heading)
Horizontal force: Measured correctly by compass
```

### Vessel Heeled (Heeling Error Present)
```
               ↑ Vertical (gravity)
                ╲
                 ╲  ┌──────────────┐
    Compass       ╲ │   COMPASS    │  ← Tilted with vessel
    frame          ╲│  ┌────────┐  │
    tilted      ────┼──│ N ? E  │  │  Vertical force now appears
                    │  │        │  │  horizontal to compass!
                    │  └────────┘  │
                    └──────────────┘
                      ╲
═══════════════════════╲═══════════ Deck (heeled)
                         ╲
                          ↓ Heel angle

Vertical dip force: Now has component in compass horizontal plane
Apparent horizontal force: Dip component + true horizontal
Result: Compass reads incorrect heading (deviation error)
```

## When Heeling Error Is Significant

### High-Risk Scenarios

**Sailing Vessel Hard on Wind:**
```
Conditions:
• Heel: 20-30°
• Consistent heel on one tack
• Extended period navigating
• Confined waters
• Critical bearings needed

Risk Level: HIGH ⚠️⚠️⚠️

Example:
Beating into harbor entrance
- Heel: 25° to starboard
- Compass reads: 045°
- True heading: possibly 040° or 050°
- Error: ±5° (significant in channel)
```

**Heavy Weather Navigation:**
```
Conditions:
• Irregular heel angles
• Rolling in seaway
• Difficult to read compass
• Stress situation

Risk Level: MODERATE-HIGH ⚠️⚠️

Example:
Storm passage near coast
- Heel: varying 15-30°
- Compass readings erratic
- Navigation critical
- Cross-check with GPS essential
```

**Racing in Fresh Breeze:**
```
Conditions:
• Sustained heel 15-25°
• Optimized for speed
• Tactical navigation
• Frequent tacking

Risk Level: MODERATE ⚠️

Example:
Coastal race, mark rounding
- Heel: 20° to port
- Approaching mark
- Bearing accuracy important
- Different compass reading each tack
```

### Low-Risk Scenarios

**Powerboat Normal Operation:**
```
Conditions:
• Heel: <5°
• Occasional rolling
• Generally level

Risk Level: LOW ✓

Heeling error typically negligible (<1-2°)
```

**Sailing Light Air:**
```
Conditions:
• Heel: 0-10°
• Gentle conditions
• Vessel relatively upright

Risk Level: LOW ✓

Heeling error minor (<2°)
```

**Downwind Sailing:**
```
Conditions:
• Heel: minimal or zero
• Rolling motion instead
• Stable heading

Risk Level: LOW ✓

Heeling error usually negligible
```

## Recognizing Heeling Error

### Symptom 1: Tack-to-Tack Heading Discrepancy

**The Test:**
1. Sail steady heading on port tack (e.g., close-hauled)
2. Note compass heading: 045°
3. Tack to starboard
4. Sail same apparent wind angle
5. Note compass heading: should be ~135° (90° difference)
6. If reading is significantly different (e.g., 140° or 130°), heeling error present

**Expected Results:**
```
NO HEELING ERROR:
Port tack:      045° compass
Starboard tack: 135° compass (90° difference)

HEELING ERROR PRESENT:
Port tack:      045° compass
Starboard tack: 142° compass (97° difference)
→ 7° discrepancy indicates heeling error
```

### Symptom 2: GPS Track vs. Compass Discrepancy

**The Test:**
1. Sail steady course while heeled
2. Note compass heading: 090°
3. Check GPS ground track: 085°
4. Difference = possible heeling error (after accounting for leeway)

**Interpretation:**
```
Compass: 090°
GPS:     085°
Leeway estimate: 5° (normal for conditions)

If leeway is 5°:
  Compass 090° - Leeway 5° = 085° expected GPS track
  GPS shows 085° → Compass is accurate ✓

If leeway should be less:
  Possible heeling error present
```

### Symptom 3: Coastline Bearing Changes Between Tacks

**The Test:**
1. Take bearing of charted object on port tack
2. Tack to starboard
3. Take bearing of same object immediately
4. Bearing should change only by your course change
5. Additional change suggests heeling error

## Estimating Heeling Error Magnitude

### Rule of Thumb
```
Heel Angle    Typical Heeling Error    Significance
─────────────────────────────────────────────────────
0-5°          0-1°                     Negligible
5-10°         1-2°                     Minor
10-15°        2-4°                     Noticeable
15-20°        3-6°                     Significant
20-25°        5-8°                     Serious
25-30°        7-12°                    Very serious
>30°          10-15°+                  Critical

Note: Varies with heading, latitude, and compass type
```

### Latitude Effect
```
Higher Latitudes (60-70°): Stronger dip → larger heeling error
Mid Latitudes (30-60°):    Moderate dip → moderate heeling error
Low Latitudes (0-30°):     Weak dip → smaller heeling error

Example:
20° heel at 60°N: might produce 8° error
20° heel at 30°N: might produce 5° error
20° heel at 10°N: might produce 3° error
```

## Mitigation Strategies

### Strategy 1: Minimize Heel During Critical Navigation

**Practical Application:**
```
BEFORE: Hard on wind, heeled 25°, entering channel
ACTION:
  1. Ease sheets 15-20%
  2. Accept 0.5-1.0 knot speed loss
  3. Reduce heel to 10-15°
  4. Take bearings
  5. Resume normal sailing after fix

BENEFIT: Reduces heeling error by 50-70%
COST: Brief speed reduction
WHEN: Channel entry, bearings, critical navigation
```

### Strategy 2: Consistent Heel Angle for Related Bearings

**Practical Application:**
```
SITUATION: Taking series of bearings for position fix

DO:
• Maintain same heel angle for all bearings
• All bearings have same error (self-consistent)
• Relative bearings more accurate
• Fix may be slightly offset but shape correct

DON'T:
• Take one bearing heeled, next upright
• Each bearing has different error
• Results inconsistent, poor fix
```

### Strategy 3: Cross-Check With GPS/Radar

**Practical Application:**
```
HEELED NAVIGATION CHECKLIST:
1. Note compass heading
2. Check GPS ground track
3. Estimate leeway (typical 5-10°)
4. Calculate: Compass - Leeway = Expected GPS track
5. Compare to actual GPS track
6. Difference suggests combined leeway and heeling error

DECISION:
• Small difference (<3°): Accept compass
• Large difference (>5°): Suspect heeling error, use GPS
```

### Strategy 4: Gimbal-Mounted Compass

**Technical Solution:**
```
FLAT-MOUNTED COMPASS:
┌────────────┐
│  Compass   │  Tilts fully with vessel
└────────────┘  Maximum heeling error
      ║
════════════════ Deck (heeled 20°)

GIMBALLED COMPASS:
    ╔════════╗
    ║Compass ║    Stays more level
    ╚════════╝    Reduced heeling error
      ⚙️ Pivot
      ║
════════════════ Deck (heeled 20°)

BENEFIT: 30-50% heeling error reduction
LIMITATION: Doesn't eliminate error
BEST FOR: Vessels regularly heeled >15°
```

### Strategy 5: Hand-Bearing Compass (Held Level)

**Practical Application:**
```
SITUATION: Taking critical bearing while heeled

TECHNIQUE:
1. Stand with clear view
2. Hold hand-bearing compass level (not tilted with vessel)
3. Use bubble level or internal gimbals
4. Keep compass horizontal regardless of vessel heel
5. Take bearing

BENEFIT: Eliminates heeling error (compass stays level)
LIMITATION: Takes practice, affected by vessel motion
BEST FOR: Position fixing, collision avoidance bearings
```

### Strategy 6: Mathematical Correction (Advanced)

**For Known Heading and Heel:**
```
Heeling error tables exist but:
• Complex (vary with heading, heel, latitude)
• Require accurate heel angle measurement
• Time-consuming to use
• Rarely practical on small vessels

BETTER APPROACH:
Use GPS/radar cross-check instead
Reserve for specific research/racing applications
```

## Decision Matrix: When to Act on Heeling Error

```
┌──────────────┬───────────────────────┬─────────────────────┐
│ Heel Angle   │ Navigation Situation  │ Action Required     │
├──────────────┼───────────────────────┼─────────────────────┤
│ 0-10°        │ Any                   │ None (negligible)   │
├──────────────┼───────────────────────┼─────────────────────┤
│ 10-15°       │ Open water            │ Monitor             │
│              │ Confined water        │ Reduce heel if able │
├──────────────┼───────────────────────┼─────────────────────┤
│ 15-20°       │ Open water            │ GPS cross-check     │
│              │ Confined water        │ Reduce heel         │
│              │ Critical bearings     │ Use hand-bearing    │
├──────────────┼───────────────────────┼─────────────────────┤
│ 20-30°       │ Any                   │ Reduce heel         │
│              │ Critical navigation   │ GPS primary         │
│              │ Bearings needed       │ Hand-bearing level  │
├──────────────┼───────────────────────┼─────────────────────┤
│ >30°         │ Any                   │ Reduce heel urgently│
│              │                       │ GPS only            │
│              │                       │ Don't trust compass │
└──────────────┴───────────────────────┴─────────────────────┘
```

## Logging Heeling Error Awareness

**Deck Log Entry Format:**
```
Time: 1430 UTC
Position: 50°15'N, 004°30'W (GPS)
Compass: 045°(C)
Heel: ~20° to starboard
Conditions: F5, beating
Note: Significant heel, compass reading may have ±5° heeling error
      GPS confirms ground track 040° (after 5° leeway estimate)
      Actual heading likely 040°(T) not 045°(T)
Action: Using GPS for primary navigation in channel approach
```

## Quick Reference Card

```
HEELING ERROR QUICK REFERENCE
──────────────────────────────────────────
RECOGNITION:
• Compass differs between tacks (same wind angle)
• GPS track differs from compass (more than leeway)
• Compass sluggish when heeled

RISK FACTORS:
• Heel >15°
• Confined waters
• Critical bearings
• Extended period heeled

MITIGATION OPTIONS:
1. Reduce heel (ease sheets temporarily)
2. Take bearings at consistent heel
3. Cross-check with GPS/radar
4. Use hand-bearing compass (held level)
5. Add safety margin to navigation

REMEMBER:
• Cannot be corrected like deviation
• Varies with every heel angle change
• More significant at higher latitudes
• When in doubt, use GPS
```
