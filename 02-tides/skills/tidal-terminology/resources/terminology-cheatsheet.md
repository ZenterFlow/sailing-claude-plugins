# Tidal Terminology Cheat Sheet

## The 8 Essential Terms (Memorize All)

### 1. Chart Datum (CD)
- **What**: Zero reference for all depths and heights
- **Where**: ≈ LAT (Lowest Astronomical Tide)
- **Use**: Basis for charted depths, drying heights, tide predictions

### 2. HAT (Highest Astronomical Tide)
- **What**: Maximum predictable water level
- **Use**: Bridge clearances (modern charts)
- **Position**: Typically 0.5-1.0m above MHWS

### 3. LAT (Lowest Astronomical Tide)
- **What**: Minimum predictable water level
- **Use**: Basis for Chart Datum
- **Position**: ≈ Chart Datum (0.0m)

### 4. MHWS (Mean High Water Springs)
- **What**: Average spring tide high water
- **Use**: Light elevations, land heights
- **Position**: Typically 0.5-1.0m below HAT

### 5. MLWS (Mean Low Water Springs)
- **What**: Average spring tide low water
- **Use**: Spring range calculation
- **Position**: Typically 0.5-1.0m above LAT

### 6. MHWN (Mean High Water Neaps)
- **What**: Average neap tide high water
- **Use**: Neap range calculation
- **Position**: Lower than MHWS

### 7. MLWN (Mean Low Water Neaps)
- **What**: Average neap tide low water
- **Use**: Neap range calculation
- **Position**: Higher than MLWS

### 8. Range
- **What**: Vertical difference between HW and LW
- **Spring**: MHWS - MLWS
- **Neap**: MHWN - MLWN
- **Specific tide**: HW height - LW height

---

## Quick Reference Formulas

### Depth Calculations
```
Total depth = Charted depth + Height of tide

Water over drying height = Height of tide - Drying height

Under-keel clearance = Total depth - Draught
```

### Range Calculations
```
Spring Range = MHWS - MLWS

Neap Range = MHWN - MLWN

Range (any tide) = HW height - LW height
```

### Clearance Calculations
```
Bridge clearance = Charted clearance + (HAT - Current tide)

Light height above water = Light elevation + MHWS - Current tide
```

---

## Datum Applications

| Feature | Datum Used | Example |
|---------|------------|---------|
| Bridge clearances | HAT (usually) | "22m" = 22m above HAT |
| Light elevations | MHWS | "15m" = 15m above MHWS |
| Charted depths | CD | "8.5" = 8.5m below CD |
| Drying heights | CD | "2.3" underlined = 2.3m above CD |
| Tide predictions | CD | "Tide 4.2m" = 4.2m above CD |

---

## Chart Symbols

### Depth (always covered)
- **Symbol**: Blue numbers (e.g., 8.5)
- **Meaning**: Meters below Chart Datum
- **Safety**: Always has this much water minimum

### Drying Height (uncovers at low tide)
- **Symbol**: Underlined numbers (e.g., 2.3)
- **Meaning**: Meters above Chart Datum
- **Safety**: Only covered when tide > drying height

### Clearance (overhead)
- **Symbol**: Magenta numbers (e.g., 22)
- **Meaning**: Meters above HAT (or MHWS on old charts)
- **Safety**: Check chart notes for datum used

---

## Vertical Hierarchy (Top to Bottom)

```
HAT     ← Maximum water level (clearances)
MHWS    ← Average spring high (lights)
MHWN    ← Average neap high
MSL     ← Approximate middle
MLWN    ← Average neap low
MLWS    ← Average spring low
LAT     ← Minimum water level
CD      ← Chart zero (≈ LAT)
```

---

## Common Exam Questions & Answers

**Q: What's the difference between CD and MSL?**
A: CD is near LAT (lowest water), MSL is middle of tidal range. CD ≠ MSL!

**Q: Why use HAT for bridges instead of MHWS?**
A: HAT is higher, provides safety margin for extreme spring tides.

**Q: Can tide go below Chart Datum?**
A: Rarely. CD ≈ LAT, which is already the lowest predictable level.

**Q: How to spot drying height on chart?**
A: Numbers are underlined (e.g., 2.3)

**Q: MHWS is 6.2m, MLWS is 0.8m. What's the range?**
A: 6.2 - 0.8 = 5.4m spring range

**Q: Which is higher: MHWN or MLWS?**
A: MHWN (neap high is higher than spring low)

**Q: What's measured from MHWS?**
A: Lights, landmarks, heights on shore

---

## Safety Minimum UKC

| Vessel Type | Minimum UKC |
|-------------|-------------|
| Power vessels | 0.5m |
| Sailing vessels | 1.0m |
| Add for: swell, squat, uncertainty | +0.5m to +1.0m |

---

## Regional Variations

**UK/Europe**: CD ≈ LAT
**USA**: Multiple datums (MLW, MLLW, etc.)
**Always**: Check chart notes for datum used!

**Irregular areas** (check almanac notes):
- Southampton (double HW)
- Solent (complex pattern)
- Poole (extended stand)
- Portland Bill (races)

---

## Memory Tricks

**Order from top**: "Happy Men Have Many Lovely Lasses"
- **H**AT
- **M**HWS
- **H**WN (M**H**WN)
- **M**LWN
- **L**WS (M**L**WS)
- **L**AT

**Spring vs Neap**:
- **S**pring = **S**ame letter (MHWS, MLWS)
- **N**eap = **N**ame letter (MHWN, MLWN)

**Clearances**:
- **HAT** = **H**eights (bridges)
- **MHWS** = **M**arks (lights)
- **CD** = **C**harted depths

---

## Pre-Passage Checklist

- [ ] Know charted depth or drying height
- [ ] Get tide height from tables
- [ ] Calculate total depth
- [ ] Check UKC = depth - draught
- [ ] Verify UKC ≥ required minimum
- [ ] Add safety margin for conditions
- [ ] Check chart datum notes
- [ ] Verify clearances if overhead obstructions

---

## Worked Example

**Scenario**: Cross bar at 1430

**Data**:
- Chart shows: "3.2" (depth) and "1.5" underlined (drying height nearby)
- Tide at 1430: 4.8m above CD
- Draught: 2.0m
- Required UKC: 0.5m

**Solution**:
```
Route 1 (over charted depth):
Total depth = 3.2 + 4.8 = 8.0m
UKC = 8.0 - 2.0 = 6.0m ✓ SAFE

Route 2 (over drying height):
Water depth = 4.8 - 1.5 = 3.3m
UKC = 3.3 - 2.0 = 1.3m ✓ SAFE (just)

Decision: Use Route 1 (more margin)
```
