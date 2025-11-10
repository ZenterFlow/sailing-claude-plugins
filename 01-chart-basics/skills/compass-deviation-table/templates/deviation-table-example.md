# Sample Deviation Table

## Standard Format Deviation Table

**Vessel:** M.V. Example
**Date Adjusted:** 15 May 2024
**Adjusted by:** J. Smith, Compass Adjuster
**Location:** Portsmouth, UK

```
╔══════════════════╦═══════════════╗
║ COMPASS HEADING  ║   DEVIATION   ║
╠══════════════════╬═══════════════╣
║      000°        ║      2°E      ║
║      015°        ║      3°E      ║
║      030°        ║      4°E      ║
║      045°        ║      4°E      ║
║      060°        ║      5°E      ║
║      075°        ║      5°E      ║
║      090°        ║      5°E      ║
║      105°        ║      5°E      ║
║      120°        ║      4°E      ║
║      135°        ║      3°E      ║
║      150°        ║      2°E      ║
║      165°        ║      1°E      ║
║      180°        ║      0°       ║
║      195°        ║      1°W      ║
║      210°        ║      2°W      ║
║      225°        ║      3°W      ║
║      240°        ║      4°W      ║
║      255°        ║      4°W      ║
║      270°        ║      4°W      ║
║      285°        ║      3°W      ║
║      300°        ║      3°W      ║
║      315°        ║      2°W      ║
║      330°        ║      2°W      ║
║      345°        ║      2°E      ║
╚══════════════════╩═══════════════╝
```

## How to Read This Table

### Example 1: Exact Match
**Compass Heading: 090°**
- Look directly in table
- 090° → 5°E
- No interpolation needed

**To convert to Magnetic:**
090°(C) + 5°E = 095°(M)

---

### Example 2: Close Approximation (within 1°)
**Compass Heading: 091°**
- Nearest entry: 090° → 5°E
- Difference: 1° (within tolerance)
- Use nearest value: 5°E

**To convert to Magnetic:**
091°(C) + 5°E = 096°(M)

---

### Example 3: Interpolation Required
**Compass Heading: 052°**
- Falls between 045° (4°E) and 060° (5°E)
- Position: (52 - 45) ÷ (60 - 45) = 7 ÷ 15 = 0.47
- Deviation: 4°E + (0.47 × 1°) = 4.5°E

**To convert to Magnetic:**
052°(C) + 4.5°E = 056.5°(M)

---

### Example 4: Crossing Zero
**Compass Heading: 172°**
- Falls between 165° (1°E) and 180° (0°)
- Position: (172 - 165) ÷ (180 - 165) = 7 ÷ 15 = 0.47
- Deviation: 1°E + (0.47 × -1°) = 0.5°E

**To convert to Magnetic:**
172°(C) + 0.5°E = 172.5°(M)

---

### Example 5: Westerly Deviation
**Compass Heading: 258°**
- Falls between 255° (4°W) and 270° (4°W)
- Both values same → 4°W (no interpolation needed)

**To convert to Magnetic:**
258°(C) - 4°W = 254°(M)

---

## Table Characteristics

### This Table Shows:
- **Maximum East Deviation**: 5°E (around 060° to 105° compass)
- **Maximum West Deviation**: 4°W (around 240° to 270° compass)
- **Zero Deviation**: 180° (south heading)
- **Deviation Pattern**: Typical for steel vessel with engine forward

### Pattern Analysis:
1. East deviation dominates easterly headings (000° to 150°)
2. West deviation dominates westerly headings (210° to 330°)
3. Transitions through zero around 180°
4. Moderate deviations (2° to 5°) – well-adjusted compass

---

## Important Notes

**⚠️ This table is ONLY valid for:**
- The ship's fixed steering compass
- Current magnetic environment on vessel
- As of adjustment date (15 May 2024)

**❌ Do NOT use this table for:**
- Hand-bearing compass readings
- Another vessel (even same class)
- If major electrical/structural changes made
- If table is >2 years old without verification

**✓ Table should be re-checked:**
- Annually by qualified compass adjuster
- After any significant electrical installation
- After structural repairs involving ferrous metals
- If compass behavior seems inconsistent

---

## Quick Lookup Guide

**Northerly Headings (000° - 090°):**
All deviations East (2°E to 5°E)

**Easterly to Southerly (090° - 180°):**
Decreasing East, through zero at 180°

**Southerly to Westerly (180° - 270°):**
Increasing West (0° to 4°W)

**Westerly to Northerly (270° - 360°):**
Decreasing West, returning to East (4°W to 2°E)

---

## Application Summary

| Conversion | Rule | Example (090°C, 5°E) |
|------------|------|----------------------|
| **C → M** | Add East, Sub West | 090° + 5° = 095°(M) |
| **M → C** | Sub East, Add West | 095° - 5° = 090°(C) |

**Memory Aid**: "Compass Add East = Magnetic" (C→M direction)
