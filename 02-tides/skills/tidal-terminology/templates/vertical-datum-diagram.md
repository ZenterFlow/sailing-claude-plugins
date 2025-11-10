## Vertical Datum Hierarchy

### Complete Vertical Reference System

```
                     ▲ Height above CD
                     │
    ┌────────────────┼────────────────┐
    │     HAT        │  +7.0m         │  Highest Astronomical Tide
    ├────────────────┼────────────────┤  ← Bridge clearances (modern charts)
    │                │                │
    │     MHWS       │  +6.2m         │  Mean High Water Springs
    ├────────────────┼────────────────┤  ← Light elevations, heights on land
    │                │                │
    │     MHWN       │  +4.8m         │  Mean High Water Neaps
    ├────────────────┼────────────────┤
    │                │                │
    ├ ─ ─ ─ ─ ─ ─ ─ ┼ ─ ─ ─ ─ ─ ─ ─ ┤  Mean Sea Level (≈+3.5m)
    │                │                │
    │     MLWN       │  +2.2m         │  Mean Low Water Neaps
    ├────────────────┼────────────────┤
    │                │                │
    │     MLWS       │  +0.8m         │  Mean Low Water Springs
    ├────────────────┼────────────────┤
    │                │                │
    │     LAT        │  +0.0m         │  Lowest Astronomical Tide
    ╞════════════════╪════════════════╡  ← Chart Datum (CD)
    │                │                │
    │  Charted Depth │  -5.2m         │  Depths below CD (blue on charts)
    │                │                │
    └────────────────┼────────────────┘
                     │  Seabed
                     ▼
```

### Key Relationships

**Spring Range** = MHWS - MLWS
```
Example: 6.2m - 0.8m = 5.4m spring range
```

**Neap Range** = MHWN - MLWN
```
Example: 4.8m - 2.2m = 2.6m neap range
```

### Practical Example: Southampton

```
    HAT        7.0m above CD
    ───────────────────────── ← Maximum water level
    MHWS       4.5m above CD  (typical spring HW)
    ───────────────────────── ← Light elevations measured from here
    MHWN       3.6m above CD  (typical neap HW)

    - - - MSL  2.3m above CD - - (approximate)

    MLWN       1.0m above CD  (typical neap LW)
    MLWS       0.5m above CD  (typical spring LW)
    LAT        0.0m           (lowest possible)
    ═══════════════════════════ Chart Datum (ZERO)

    Seabed    -12.3m          (charted depth 12.3m)
```

### Understanding the Diagram

**Above Chart Datum (+)**: Water levels, tidal heights
- All tide predictions given as "height above CD"
- Example: "Tide height 4.2m" means 4.2m above Chart Datum

**Below Chart Datum (-)**: Charted depths
- Blue numbers on charts show depth below CD
- Example: "8.5" on chart means 8.5m below CD
- Always has water (even at LAT ≈ CD)

**At Chart Datum (0)**: The reference plane
- Starting point for all measurements
- Set at approximately LAT for safety

### Drying Heights vs Charted Depths

```
         Tide at MHWS
         │
    ┌────▼────┐
    │ Water   │ 4.5m above CD
    │         │
    ╞═════════╡ CD (0.0m)
    │         │
    │ Always  │ 3.2m below CD (charted depth)
    │ covered │
    └─────────┘ Seabed

    vs

         Tide at MLWS
         │
         ▼
    ┌────┬────┐
    │    │    │ 0.8m above CD
    ╞════╧════╡ CD (0.0m)
    │ Drying  │
    │  rock   │ 1.5m above CD (drying height)
    │ exposed │ (underlined on chart)
    └─────────┘ Rock top
```

**Key Difference**:
- **Charted depth** (5.2): Always covered, 5.2m below CD
- **Drying height** (1.5 underlined): Uncovers at low tide, 1.5m above CD

### Clearances and Elevations

**Bridge Clearance** (measured from HAT or MHWS):
```
    Bridge deck
    ═══════════════════════
         ↕ 22m clearance
    ───────────────────────── HAT (7.0m above CD)
                              (or MHWS on older charts)
         Water
    ═══════════════════════ CD
```

**Actual clearance at any tide**:
```
At spring HW (4.5m above CD):
Actual clearance = 22m + (7.0 - 4.5) = 24.5m

At neap HW (3.6m above CD):
Actual clearance = 22m + (7.0 - 3.6) = 25.4m

At CD (0.0m):
Actual clearance = 22m + 7.0 = 29.0m
```

**Light Elevation** (measured from MHWS):
```
    Light → ⚪ 15m above MHWS
              ↕
    ───────────────────────── MHWS (6.2m above CD)

         Water level

    ═══════════════════════ CD

Total height of light above CD = 15 + 6.2 = 21.2m
```

### Memory Aid

**Top to Bottom**:
- **H**AT = **H**ighest (maximum possible)
- **MHWS** = Mean **H**igh **W**ater **S**prings (average spring high)
- **MHWN** = Mean **H**igh **W**ater **N**eaps (average neap high)
- MSL = Mean **S**ea **L**evel (middle, approximate)
- **MLWN** = Mean **L**ow **W**ater **N**eaps (average neap low)
- **MLWS** = Mean **L**ow **W**ater **S**prings (average spring low)
- **L**AT = **L**owest (minimum possible)
- CD = Chart Datum (≈ LAT, ZERO reference)

**Applications**:
- **HAT** → Bridge clearances (usually)
- **MHWS** → Light elevations
- **CD** → All charted depths, drying heights
- **Range** → MHWS - MLWS (spring) or MHWN - MLWN (neap)
