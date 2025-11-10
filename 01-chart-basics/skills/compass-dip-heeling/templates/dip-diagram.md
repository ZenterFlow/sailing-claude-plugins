# Magnetic Dip Visual Guide

## Earth's Magnetic Field Structure

```
                    GEOGRAPHIC NORTH POLE
                           (90°N)
                             |
                             |
        ╔════════════════════╪════════════════════╗
        ║                    |                    ║
        ║         NORTHERN HEMISPHERE             ║
        ║                    |                    ║
        ║    Field lines     |    Field lines    ║
        ║    angle DOWN   ←──┼──→   angle DOWN   ║
        ║    into Earth      |      into Earth   ║
        ║                    |                    ║
    ════╬════════════ MAGNETIC EQUATOR ══════════╬════
        ║              (Aclinic Line, 0° dip)    ║
        ║                    |                    ║
        ║    Field lines     |    Field lines    ║
        ║    angle DOWN   ←──┼──→   angle DOWN   ║
        ║    (from above)    |    (from above)   ║
        ║                    |                    ║
        ║         SOUTHERN HEMISPHERE             ║
        ║                    |                    ║
        ╚════════════════════╪════════════════════╝
                             |
                             |
                    GEOGRAPHIC SOUTH POLE
                           (90°S)

        Magnetic South Pole ←─┘         └─→ Magnetic North Pole
           (near 64°S, 136°E)              (near 86°N, 160°W)
```

## Dip Angle at Different Latitudes

### Northern Hemisphere View (Cross-Section)
```
                        ↑ Surface Level
    ──────────────────────────────────────────
                        │
                        │  Compass needle tries to align
         North end  ┌───┼───┐  with field lines
         pulled     │   ↓   │  (angle = dip)
         downward   └───────┘
                        ║
                        ║ Magnetic field line
                        ║ (angles downward)
                        ║
                        ▼ Into Earth

High Latitude (70°N): Field line angle ~70° from horizontal
Mid Latitude (50°N):  Field line angle ~65° from horizontal
Low Latitude (20°N):  Field line angle ~40° from horizontal
```

### Southern Hemisphere View (Cross-Section)
```
                        ↑ Surface Level
    ──────────────────────────────────────────
                        ║
                        ║ Magnetic field line
                        ║ (angles downward from above)
                        ║
         South end  ┌───┼───┐  Compass needle tries to align
         pulled     │   ↓   │  with field lines
         downward   └───────┘  (angle = dip)
                        │
                        │
                        ▼ Into Earth (from above)

High Latitude (70°S): Field line angle ~70° from horizontal
Mid Latitude (50°S):  Field line angle ~65° from horizontal
Low Latitude (20°S):  Field line angle ~40° from horizontal
```

## Global Dip Angle Map

```
       90°N ─┐
             │  DIP: +85° to +90°  ← North Magnetic Pole region
       80°N ─┤      (Vertical, straight down)
             │
       70°N ─┤  DIP: +70° to +80°
             │      (Steep angle downward)
       60°N ─┤
             │  DIP: +60° to +70°  ← Northern Zone 1-2
       50°N ─┤      (Strong downward angle)
             │
       40°N ─┤  DIP: +50° to +60°  ← Northern Zone 2-3
             │      (Moderate angle)
       30°N ─┤
             │  DIP: +35° to +50°
       20°N ─┤      (Gentle angle)
             │
       10°N ─┤  DIP: +15° to +30°  ← Equatorial Zone 3
             │      (Slight angle)
EQUATOR ═════╪═════ DIP: 0° ←─── Aclinic Line (horizontal)
       10°S ─┤  DIP: -15° to -30°
             │      (Slight angle from above)
       20°S ─┤
             │  DIP: -35° to -50°
       30°S ─┤      (Gentle angle from above)
             │
       40°S ─┤  DIP: -50° to -60°  ← Southern Zone 3-4
             │      (Moderate angle)
       50°S ─┤
             │  DIP: -60° to -70°  ← Southern Zone 4-5
       60°S ─┤      (Strong angle from above)
             │
       70°S ─┤  DIP: -70° to -80°
             │      (Steep angle from above)
       80°S ─┤
             │  DIP: -85° to -90°  ← South Magnetic Pole region
       90°S ─┘      (Vertical, straight down from above)
```

## Compass Needle Behavior by Location

### At Magnetic North Pole (+90° dip)
```
    Surface
    ───────────
        │
        │ Needle wants to
        │ point straight down
        ↓
    Unusable for navigation
```

### Northern Hemisphere (e.g., UK, +67° dip)
```
    Surface
    ───────────
            ╱
    ┌─────╱────┐  North end pulled
    │    ╱     │  down at 67° angle
    │   N      │
    └──────────┘

    WITHOUT BALANCE: Card drags, sluggish
    WITH BALANCE: North end weighted to stay level
```

### Magnetic Equator (0° dip)
```
    Surface
    ───────────

    ┌───N───E───┐  Field lines horizontal
    │           │  No vertical pull
    └───────────┘

    Compass naturally level, works any hemisphere
```

### Southern Hemisphere (e.g., Sydney, -65° dip)
```
    Surface
    ───────────
    ┌──────────┐
    │      S   │  South end pulled
    │     ╱    │  down at 65° angle
    └────╱─────┘
        ╱

    WITHOUT BALANCE: Card drags, sluggish
    WITH BALANCE: South end weighted to stay level
```

## Compass Balancing Solutions

### Unbalanced Northern Hemisphere Compass
```
    In Northern Hemisphere:
    ───────────────────────
         WORKS ✓
    ┌────[W]────┐  Weight on north end
    │    N      │  counteracts dip pull
    └───────────┘
    Card stays level

    In Southern Hemisphere:
    ───────────────────────
         FAILS ✗
    ┌────[W]────┐  Weight wrong end
    │    N  ╲   │  Exaggerates problem
    └──────┼─╲──┘  Double downward pull
           ↓  ╲   Card binds/sluggish
```

### Unbalanced Southern Hemisphere Compass
```
    In Southern Hemisphere:
    ───────────────────────
         WORKS ✓
    ┌───────────┐
    │      S[W] │  Weight on south end
    └───────────┘  counteracts dip pull
    Card stays level

    In Northern Hemisphere:
    ───────────────────────
         FAILS ✗
    ┌───────────┐
    │   ╱  S[W] │  Weight wrong end
    └──╱─┼──────┘  Exaggerates problem
      ╱  ↓        Double downward pull
              Card binds/sluggish
```

### Global/Universal Compass
```
    Anywhere:
    ───────────────────────
         ACCEPTABLE ✓
    ┌───────────┐
    │  [Special │  Complex pivot design
    │   Pivot]  │  works all latitudes
    └───────────┘

    Trade-offs:
    • More expensive
    • Not as accurate as zone-specific
    • Good enough for most navigation
    • Essential for world cruising
```

## Isoclinic Lines Concept

```
ISOCLINIC LINES = Lines of equal dip angle

Example: The +60° Isoclinic Line

    Atlantic Ocean View:

    60°W   40°W   20°W    0°    20°E   40°E
     │      │      │      │      │      │
─────┼──────┼──────┼──────┼──────┼──────┼───── 60°N
     │      │      │      │      │      │
     │  ≈═══════════+60° LINE════════╗  │
     │      │      │      │      │   ║  │
─────┼──────┼──────┼──────┼──────┼───╬──┼───── 50°N
     │      │      │      │      │   ║  │
     │      │      │      │      │   ╚══╬═
     │      │      │      │      │      ╬─── Dip angle = 60°
─────┼──────┼──────┼──────┼──────┼──────╬───── 40°N
     │      │      │      │      │      │ all along this line

Key Points:
• Isoclinic lines roughly parallel to magnetic equator
• Do NOT exactly follow latitude lines
• Earth's field is irregular
• Compass zones designed around isoclinic bands
```

## Aclinic Line (Magnetic Equator)

```
ACLINIC LINE = 0° Dip (field horizontal)

Approximate position (varies by longitude):

    160°W 120°W 80°W  40°W   0°   40°E  80°E 120°E 160°E
      │     │    │     │     │     │     │     │     │
──────┼─────┼────┼─────┼─────┼─────┼─────┼─────┼─────┼──── 10°N
      │     │    │     │     │     │     │     │     │
═════════════════════ ACLINIC LINE ═══════════════════════ ~0-5°N
      │     │    │     │     │     │     │     │     │     (varies)
──────┼─────┼────┼─────┼─────┼─────┼─────┼─────┼─────┼──── 10°S
      │     │    │     │     │     │     │     │     │
    Pacific   Americas      Atlantic    Africa   Asia   Pacific

Characteristics:
• Roughly follows geographic equator
• Drifts 0-5° north/south by longitude
• Zero vertical magnetic force
• Compasses from either hemisphere work acceptably
• Transition zone between hemisphere requirements
```

## Practical Compass Zone Reference

```
COMPASS ZONE SYSTEM (typical manufacturer zones)

Zone 1: 60°N-90°N     Strong northern balance    │
Zone 2: 30°N-60°N     Moderate northern balance  │ Northern
Zone 3: 20°S-30°N     Universal/Equatorial       │ Hemisphere
───────────────────────────────────────────────────────────
Zone 3: 20°S-30°N     Universal/Equatorial       │
Zone 4: 20°S-60°S     Moderate southern balance  │ Southern
Zone 5: 60°S-90°S     Strong southern balance    │ Hemisphere

Common Regional Requirements:
• UK, North Europe: Zone 2
• Mediterranean, Southern US: Zone 2-3
• Caribbean, Central America: Zone 3
• Australia, New Zealand: Zone 4
• Southern Ocean: Zone 4-5
```

## Visual Summary: Why Dip Matters

```
SCENARIO: UK boat (Zone 2 compass) sails to Australia

    In UK (55°N, +67° dip):
    ───────────────────────
    ┌────[W]────┐  Weight counteracts
    │  N ═══ E  │  northern dip pull
    │           │  COMPASS ACCURATE ✓
    └───────────┘

    In Australia (35°S, -60° dip):
    ───────────────────────
    ┌────[W]────┐  Weight now reinforces
    │  N   ╲    │  southern dip pull
    │   ╲  S    │  COMPASS SLUGGISH ✗
    └────╲──────┘  Drag, slow response
          ↓↓       Navigation unreliable

ACTION REQUIRED:
Replace with Zone 4 compass (southern hemisphere balanced)
```
