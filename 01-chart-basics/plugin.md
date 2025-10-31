# Chart Basics Plugin

**RYA/ASA Yachtmaster – Chart Fundamentals, Datums, Symbols & Compass**

## Purpose
Master the foundational chart-work skills: understanding chart datums (depth & geodetic), reading symbols, Mercator projection principles, and compass error corrections (variation & deviation).

## Activation Triggers
- "Chart datum explained"
- "Can I plot WGS-84 on this chart?"
- "What does this symbol mean?"
- "Datum shift for [chart number]"
- "Charted height above what?"
- "Test me on chart symbols"
- "GPS datum vs chart datum"
- "Variation and deviation"

## Topics Covered

### 1. Geodetic Datums (GPS ↔ Chart)
**Purpose**: Prevent 0.5+ NM position errors from datum mismatches

**Skills**:
- Identify chart's geodetic datum (WGS-84, ED-50, NAD-27, etc.)
- Calculate position shift when GPS datum ≠ chart datum
- Apply corrections before plotting GPS positions

**Common Scenarios**:
- "GPS is WGS-84, chart is ED-50" → Apply 0.3-0.5' shift
- "Can I plot WGS-84 straight onto BA 2454?" → Check compatibility
- UK charts: max ~0.5 NM shift; elsewhere can exceed 1 NM

### 2. Vertical Datums (Heights & Depths)
**Purpose**: Understand what "height" means on charts

**Depth References**:
- **Chart Datum (CD)**: Soundings/depths shown (usually LAT in UK)
- **LAT** (Lowest Astronomical Tide): UK/EU standard
- **MLLW** (Mean Lower Low Water): US/Canada standard
- **Drying heights**: Above CD, uncovered at low tide

**Height References**:
- **HAT** (Highest Astronomical Tide): UK bridge clearances
- **MHWS** (Mean High Water Springs): Some overhead features
- **MSL** (Mean Sea Level): Land contours, spot heights

**Skills**:
- State which datum a charted height references
- Regional differences (UK vs US vs AUS)
- Convert between datums for safety calculations

### 3. Chart Symbols & Abbreviations
**Purpose**: Rapid identification of chart features per INT 1 / 5011

**Learning Modes**:
- **Quiz Mode**: Flash cards with multiple choice
- **Lookup Mode**: "What does this symbol mean?"
- **Practice Mode**: Timed symbol recognition

**Symbol Categories**:
- Navigational aids (lights, buoys, beacons)
- Depths & seabed (rock, wreck, kelp, coral)
- Coastline features (cliffs, beaches, structures)
- Port facilities (pier, marina, harbor)
- Dangers (overhead cables, restricted areas)

**Features**:
- 100+ common symbols from INT 1 / Chart 5011
- Session scoring and progress tracking
- Explanations with context ("Why is this important?")

### 4. Mercator Projection Basics
**Purpose**: Understand why distances distort with latitude

**Key Concepts**:
- Scale varies with latitude (1 NM ≠ constant cm)
- Use latitude scale for measuring distance
- Why rhumb lines appear straight
- Great circle vs rhumb line distances

### 5. Compass Errors
**Purpose**: Calculate True ↔ Magnetic ↔ Compass conversions

**Variation**:
- Magnetic declination from true north
- Read from compass rose on chart
- Annual change rate (e.g., "3°W 2024, decreasing 8' annually")

**Deviation**:
- Ship's magnetic field affecting compass
- Deviation card lookup by heading
- Combining variation + deviation

**Formulas**:
- True → Magnetic: Apply Variation
- Magnetic → Compass: Apply Deviation
- Memory aids: "CADET" (Compass → True: Add East)

## Workflow

### Initial Assessment
1. User asks chart-related question
2. Plugin identifies topic (datum, symbol, compass, projection)
3. Activates appropriate skill module

### Interactive Learning
- **Datum questions**: Look up chart, calculate shift, provide worked example
- **Symbol questions**: Show symbol, give multiple choice or explanation
- **Compass questions**: Step-by-step T↔M↔C conversion with memory aids

### Validation
- Provide worked examples for each calculation
- Flag common errors (e.g., "Did you add East or West?")
- Link to official references (INT 1, 5011, Admiralty guides)

## Resources Included
- Geodetic datum shift table (150+ charts)
- Vertical datum reference guide (UK/US/AUS/NZ)
- Chart symbol deck (100+ symbols with images)
- Variation/deviation calculation templates
- Sample exam questions with answers

## Quality Checklist
- [ ] Datum shift calculated correctly (within 0.1')
- [ ] Vertical datum stated with regional note
- [ ] Symbol identified per INT 1 / 5011
- [ ] Compass conversion shows all steps
- [ ] Units and references clearly stated
- [ ] Common errors flagged proactively

## Integration Notes
- Links to **Plugin 02 (Tides)** for height calculations
- Links to **Plugin 03 (Positioning)** for plotting positions
- Links to **Plugin 09 (Pilotage)** for chart updating
- Provides foundation for all navigation calculations

## Example Sessions

### Example 1: Geodetic Datum Check
**User**: "Can I plot WGS-84 straight onto BA 2454?"

**Plugin Response**:
```
✅ SAFE TO PLOT

BA 2454 (Approaches to Portsmouth) uses WGS-84 geodetic datum.
Your GPS is also WGS-84.

→ No shift required - plot position directly as read from GPS.

Note: Always check chart title block for datum before plotting.
```

### Example 2: Datum Mismatch
**User**: "GPS is WGS-84, chart is ED-50 (BA 1876). What shift do I apply?"

**Plugin Response**:
```
⚠️ DATUM MISMATCH - APPLY SHIFT BEFORE PLOTTING

Chart: BA 1876 (Alderney to Cap de la Hague)
Chart Datum: European Datum 1950 (ED-50)
GPS Datum: WGS-84

Required Shift: 0.3' N, 0.1' W (~370m total)

Worked Example:
GPS Position: 49° 42.5' N, 002° 15.3' W
Apply Shift:  + 0.3' N,   - 0.1' W
Plot at:      49° 42.8' N, 002° 15.4' W

⚠️ Failure to apply this shift could put you 370m from your actual position!
```

### Example 3: Vertical Datum
**User**: "Is that lighthouse height above HAT or MHWS?"

**Plugin Response**:
```
LIGHTHOUSE HEIGHT DATUM (UK Charts)

Object Type: Lighthouse (structure height)
Region: UK / European waters
Datum: Mean High Water Springs (MHWS)

Why: Land features and structures shown above MHWS.
Tide can reach higher (up to HAT) in exceptional conditions.

Clearance heights (bridges, wires): Above HAT (more conservative)

Quick Reference:
- Structure heights (lighthouses, cliffs): MHWS
- Bridge vertical clearances: HAT
- Depths & drying heights: Chart Datum (LAT)
- Land contours: Mean Sea Level (MSL)
```

### Example 4: Symbol Quiz
**User**: "Test me on chart symbols"

**Plugin Response**:
```
🎯 CHART SYMBOL QUIZ - Question 1/10

What does this symbol mean?

    ⚓
   (3)

A) Anchorage, maximum depth 3m
B) Anchor prohibited, 3 cables radius
C) Anchorage, depth 3 fathoms
D) Anchoring area, 3 vessels max

[Type A, B, C, or D]
```

**User**: "A"

**Plugin Response**:
```
❌ Not quite!

Correct Answer: C - Anchorage, depth 3 fathoms

Explanation:
- ⚓ symbol = designated anchorage
- (3) in parentheses = depth in FATHOMS (not metres)
- 3 fathoms = 18 feet = 5.5 metres

Common Confusion:
- Depths in parentheses () = fathoms/feet
- Depths underlined = metres
- Always check chart's depth unit (title block)

Score: 0/1 | Next question?
```

### Example 5: Compass Conversion
**User**: "Convert 085°T to compass heading. Variation 5°W, deviation +2°E"

**Plugin Response**:
```
COMPASS CONVERSION: True → Compass

Given:
- True Course: 085°T
- Variation: 5°W (2024)
- Deviation: +2°E (on heading ~085°)

Step 1: True → Magnetic
085°T + 5° (subtract West variation) = 080°M

Step 2: Magnetic → Compass
080°M - 2° (subtract East deviation) = 078°C

Answer: Steer 078° on the ship's compass

Memory Aid "CADET":
Compass → True: Add East
(Going opposite direction, reverse the operations)

Verification:
078°C + 2°E = 080°M
080°M + 5°W = 085°T ✓
```

## Version History
- **v0.1.0** (2025-10-31): Initial plugin with 4 core skills (datum-guardian, charted-height-interpreter, symbol-spotter, compass-converter)
