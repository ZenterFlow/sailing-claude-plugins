---
name: compass-deviation-table
description: Read and apply ship's compass deviation table with interpolation for headings between table values.
license: CC-BY-SA
---

# SKILL: compass-deviation-table
**RYA Yachtmaster – Using the Ship's Compass Deviation Table**

## Purpose
Teach students how to read, interpret, and apply the vessel's deviation table, including interpolation between table entries for accurate compass-to-magnetic conversions.

## Activation Triggers
- "Read deviation table"
- "Deviation for heading"
- "Interpolate deviation"
- "What's the deviation at 081°"
- "Use deviation table"
- "Ship's compass deviation"
- "Compass heading 125°, what deviation"

## Behaviour
1. Explain deviation table structure:
   - Left column: Compass headings (typically 15° or 30° increments)
   - Right column: Deviation values with East (E) or West (W)
   - Ship-specific: Only applies to fixed ship's compass

2. Determine if interpolation is needed:
   - Exact match: Use table value directly
   - Between values: Interpolate proportionally
   - Threshold: Interpolate if difference > 1° from nearest value

3. Apply interpolation when needed:
   - Find bracketing table entries
   - Calculate proportional position
   - Interpolate deviation value
   - Round to nearest 0.5° or 1° as appropriate

4. Apply deviation correctly:
   - **Compass → Magnetic**: Add East, Subtract West
   - **Magnetic → Compass**: Subtract East, Add West
   - Always check table entry for current compass heading
   - Explain why deviation doesn't apply to hand-bearing compass

5. Show complete working:
   - Display table entries used
   - Show interpolation calculation if applicable
   - Apply deviation with clear sign convention
   - State final result with label (C) or (M)

## File Map
- `manifest.json` – skill metadata
- `instructions.md` – full instructor prompt for deviation tables
- `templates/deviation-table-example.md` – sample deviation table format
- `templates/interpolation-guide.md` – how to interpolate between values
- `tests/sample-prompts.md` – validation test cases
- `resources/sample-tables.md` – example deviation tables from different vessels

## Example Session

**User:** "My compass heading is 081°. What's the deviation from this table?"

**Skill displays table:**
```
Compass Heading | Deviation
000°           | 2°E
045°           | 3°E
090°           | 5°E
135°           | 6°E
```

**Skill:**
```
DEVIATION TABLE LOOKUP: 081°(C)

Table Analysis:
- 081° falls between 045° and 090°
- At 045°: Deviation = 3°E
- At 090°: Deviation = 5°E
- Difference span: 90° - 45° = 45°

Interpolation Required:
- Target: 081° (between 045° and 090°)
- Position: 081° - 045° = 36° into the range
- Proportion: 36° ÷ 45° = 0.80 (80% of the way)

Deviation Calculation:
- Range: 3°E to 5°E (2° difference)
- Interpolated deviation: 3°E + (0.80 × 2°) = 4.6°E
- Rounded: 5°E

✅ DEVIATION at 081°(C): 5°E

To convert to Magnetic:
081°(C) + 5°E = 086°(M)
```

**User:** "What about 090° exactly?"

**Skill:**
```
DEVIATION TABLE LOOKUP: 090°(C)

Exact Match Found:
- 090° appears directly in table
- Deviation = 5°E

✅ DEVIATION at 090°(C): 5°E (no interpolation needed)

To convert to Magnetic:
090°(C) + 5°E = 095°(M)
```

**User:** "If I want to steer 120°(M), what compass heading should I use?"

**Skill:**
```
MAGNETIC → COMPASS CONVERSION

Given: 120°(M)
Need: Compass heading

Process:
1. Estimate compass heading (close to 120°)
2. Find deviation for compass heading near 115-120°

Table Check for ~115°:
- Between 090° (5°E) and 135° (6°E)
- At 115°: approximately 5.5°E

Apply Reverse Deviation (M→C):
- Rule: Subtract East when going M→C
- 120°(M) - 5.5°E ≈ 114.5°(C)

Verify:
- Check deviation at 115°(C) = 5.5°E
- 114.5°(C) + 5.5°E = 120°(M) ✓

✅ STEER: 115°(C) to achieve 120°(M)
```

## Key Concepts
- **Deviation is heading-dependent**: Changes with ship's heading
- **Ship's compass only**: Hand-bearing compass has no deviation
- **Interpolation threshold**: Use when >1° from table entry
- **Table validity**: Only valid for ship's current magnetic environment
- **C→M vs M→C**: Direction matters for applying deviation
- **Accuracy**: Round to 0.5° or 1° – false precision is meaningless

## Safety Notes
- **Always use current table**: Deviation changes if electrical/metal equipment added
- **Check table date**: Should be verified annually by compass adjuster
- **Single-figure accuracy**: Interpolation gives 1° accuracy at best
- **Hand-bearing compass**: Use magnetic bearings directly – no deviation table
