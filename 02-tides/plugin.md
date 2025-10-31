# Tides Plugin

**RYA/ASA Yachtmaster – Complete Tidal Calculations Suite**

## Purpose
Master all tidal calculations for safe navigation: heights, times, secondary ports, rule-of-twelfths, tidal streams, tidal diamonds, and depth/clearance safety checks.

## Activation Triggers
- "Calculate tide at [port]"
- "Tide height at [time]"
- "Secondary port tide"
- "When will tide reach [height]"
- "Rule of twelfths"
- "Tidal stream rate"
- "Diamond [letter] at HW+[hours]"
- "Will I touch bottom?"
- "Bridge clearance at [tide]"
- "Drying height calculation"

## Topics Covered

### 1. Tidal Height Calculations (Primary Ports)
**Method**: Admiralty tidal curves + rule-of-twelfths

**Inputs**:
- Port name (e.g., Plymouth, Dover, Portsmouth)
- Date & time (UTC or local with timezone)
- Required: height at time OR time when tide reaches specific height

**Calculations**:
- HW/LW times from tide tables
- Range (HW height - LW height)
- Duration (time between HW and LW)
- Interpolation using tidal curve or rule-of-twelfths
- Height above Chart Datum at any time

**Output Format**:
```
Tide at Plymouth, 2025-06-15, 14:30 UTC

HW: 18:05 UTC at 5.2m CD
LW: 11:45 UTC at 1.1m CD
Range: 4.1m
Duration: 6h 20m

Time from LW: 2h 45m (43% of duration)
Height: 2.8m above Chart Datum

Method: Tidal curve (preferred)
Chart Datum: LAT (Lowest Astronomical Tide)
```

### 2. Secondary Port Corrections
**Method**: Apply time and height differences to reference port

**Process**:
1. Identify reference (standard) port
2. Look up HW/LW times and heights for reference port
3. Apply time differences (±minutes)
4. Apply height differences (±metres or ratio)
5. Calculate range and apply rule-of-twelfths/curve

**Common Secondary Ports**:
- Dover (ref: Dover) - often IS the reference
- Fowey (ref: Plymouth)
- St Peter Port (ref: St Helier)
- Wicklow (ref: Cobh)

**Output Shows**:
- Reference port data
- Differences applied
- Final HW/LW times and heights
- Full workings for exam/verification

### 3. Rule of Twelfths
**Quick Method**: When tidal curve not available

**Rule**:
- 1st hour: 1/12 of range
- 2nd hour: 2/12 of range
- 3rd hour: 3/12 of range
- 4th hour: 3/12 of range
- 5th hour: 2/12 of range
- 6th hour: 1/12 of range

**Pattern**: 1-2-3-3-2-1 (symmetrical)

**Limitations**:
- Assumes 6-hour tidal cycle
- Less accurate than tidal curve
- Not suitable for irregular tides (Solent, Poole, Victoria BC)
- Use for quick estimates only

### 4. Tidal Streams & Tidal Diamonds
**Purpose**: Predict set (direction) and drift (speed) of tidal current

**Tidal Diamond Reading**:
- Input: Diamond letter (A-Z on chart)
- Input: Hours relative to HW at reference port (HW-6 to HW+6)
- Input: Springs or Neaps
- Output: Set (°T) and drift (knots)

**Computation of Rates**:
- Springs data: Use as given
- Neaps data: Use as given
- Between springs/neaps: Interpolate linearly
- Formula: Rate = Neaps + (Springs - Neaps) × (Range - Neap Range) / (Spring Range - Neap Range)

**Stream Atlas**:
- Alternative to tidal diamonds
- Shows streams across entire area
- Keyed to HW at standard port
- More visual, less precise than diamonds

### 5. Depth Safety Calculations
**Purpose**: Ensure sufficient under-keel clearance

**Formula**:
```
Available Depth = Charted Sounding + Tide Height
Required Depth = Draught + Under-Keel Clearance

SAFE if Available ≥ Required
```

**Under-Keel Clearance (UKC)**:
- Power vessels: 0.5m minimum
- Sailing vessels: 1.0m minimum (keel vulnerability)
- Rough seas: Add 0.5-1.0m extra
- Restricted channels: Add margin for squat

**Drying Heights**:
```
Water Depth = Tide Height - Drying Height

If negative → area is DRY (exposed)
If positive → available depth shown

Example:
Drying 1.2m, tide at 2.5m CD
→ Water depth = 2.5 - 1.2 = 1.3m
→ Available for 1.0m draught with 0.3m UKC
```

### 6. Vertical Clearance Calculations
**Purpose**: Ensure mast/aerial won't hit bridge or overhead cable

**Formula**:
```
Available Clearance = Charted Height + Tide Height
Required Clearance = Mast Height

HIT if Available < Required
SAFE if Available ≥ Required
```

**Important Notes**:
- Charted heights above HAT (UK) or MHWS
- Tide height ADDS to clearance (higher tide = more clearance)
- Opposite of depth calculations!
- Include margin for:
  - Heel (sailing)
  - Squat (high speed)
  - Swell/waves
  - Antenna/equipment on mast

**Example**:
```
Bridge: 22.0m above HAT
Tide: +1.2m above HAT
Mast: 19.5m

Available = 22.0 + 1.2 = 23.2m
Required = 19.5m
Clearance = 23.2 - 19.5 = 3.7m SAFE
```

## Workflow

### Tidal Height Query
1. User provides port, date, time
2. Plugin looks up tide tables (or asks user for HW/LW data)
3. Calculates using curve or twelfths
4. Shows full workings
5. States datum and warns of irregular tides if applicable

### Tidal Stream Query
1. User provides diamond letter, hour, springs/neaps
2. Plugin retrieves diamond data
3. Applies computation-of-rates if between springs/neaps
4. Returns set (°T) and drift (knots)
5. Reminds to apply ±1 hour either side

### Safety Check Query
1. User provides: draught, clearance desired, charted depth/height, current tide
2. Plugin calculates available vs required
3. Returns: SAFE / CAUTION / GROUNDING / MAST HIT
4. Shows actual UKC or clearance margin
5. Flags concerns (low UKC, high risk)

## Resources Included
- Rule-of-twelfths reference table
- Secondary port difference tables (50+ UK/EU ports)
- Tidal diamond lookup database
- Sample tidal curves (visual reference)
- Computation-of-rates calculation template
- Worked examples for all calculation types

## Quality Checklist
- [ ] All times stated with timezone (UTC/BST/local)
- [ ] Heights stated with datum (CD, LAT, HAT, MHWS)
- [ ] Full workings shown for verification
- [ ] Irregular tides flagged (Solent, Poole, Victoria BC, Southampton)
- [ ] UKC/clearance margin explicitly stated
- [ ] Safety assessment color-coded (SAFE/CAUTION/DANGER)
- [ ] Method stated (curve vs twelfths)
- [ ] Range and duration calculated correctly

## Integration Notes
- Links to **Plugin 01 (Chart Basics)** for datum explanations
- Links to **Plugin 03 (Positioning)** for EP with tidal stream
- Links to **Plugin 04 (Course to Steer)** for stream corrections
- Links to **Plugin 07 (Passage Making)** for tidal planning

## Example Sessions

### Example 1: Primary Port Height
**User**: "What is the tide height at Portsmouth at 14:30 on 15 June 2025?"

**Plugin Response**:
```
🌊 TIDAL HEIGHT CALCULATION

Port: Portsmouth (Primary Port)
Date: 2025-06-15
Time: 14:30 UTC

Tide Data (from Admiralty tables):
- HW: 11:25 UTC at 4.7m CD
- LW: 17:50 UTC at 1.2m CD

Calculation:
Range = 4.7 - 1.2 = 3.5m
Duration = 17:50 - 11:25 = 6h 25m

Time from HW = 14:30 - 11:25 = 3h 05m
Time from LW = 17:50 - 14:30 = 3h 20m

Using tidal curve (Portsmouth):
- Time: 3h 05m after HW (48% of duration falling)
- Height drop: ~2.2m
- Height at 14:30 = 4.7 - 2.2 = 2.5m CD

📊 RESULT: 2.5m above Chart Datum

Method: Admiralty tidal curve (preferred over twelfths)
Datum: Chart Datum (LAT - Lowest Astronomical Tide)
```

### Example 2: Secondary Port
**User**: "Calculate HW time and height at Fowey on 20 July 2025"

**Plugin Response**:
```
🌊 SECONDARY PORT CALCULATION

Secondary Port: Fowey
Reference Port: Plymouth (Devonport)
Date: 2025-07-20

Step 1: Plymouth HW Data
- HW: 08:15 UTC at 5.1m CD
- LW: 14:40 UTC at 1.3m CD

Step 2: Fowey Differences (from Admiralty tables)
Time Difference: -0025 (25 minutes earlier)
Height Ratio: ×0.95

Step 3: Apply Corrections
Fowey HW Time = 08:15 - 0:25 = 07:50 UTC
Fowey HW Height = 5.1 × 0.95 = 4.8m CD

📊 RESULT:
Fowey HW: 07:50 UTC at 4.8m CD

Reference: Plymouth (Devonport)
Method: Secondary port correction
Use this data for further twelfths/curve calculations
```

### Example 3: Rule of Twelfths
**User**: "Using rule of twelfths: HW 18:00 at 5.2m, LW 12:00 at 1.2m. What height at 15:30?"

**Plugin Response**:
```
🌊 RULE OF TWELFTHS CALCULATION

HW: 18:00 at 5.2m CD
LW: 12:00 at 1.2m CD
Query: 15:30

Step 1: Calculate Range
Range = 5.2 - 1.2 = 4.0m
1/12th = 4.0 ÷ 12 = 0.33m

Step 2: Time from LW
15:30 - 12:00 = 3h 30m (between LW and HW)

Step 3: Apply Rule (rising tide)
1st hour (12:00-13:00): +1/12 = +0.33m → 1.53m
2nd hour (13:00-14:00): +2/12 = +0.67m → 2.20m
3rd hour (14:00-15:00): +3/12 = +1.00m → 3.20m
4th hour (15:00-16:00): +3/12 = +1.00m → 4.20m

At 15:30 (halfway through 4th hour):
3.20m + (1.00 ÷ 2) = 3.20 + 0.50 = 3.70m CD

📊 RESULT: 3.70m above Chart Datum

Method: Rule of Twelfths (use curve if available for better accuracy)
Pattern: 1-2-3-3-2-1 (symmetrical)
```

### Example 4: Tidal Diamond
**User**: "Diamond F, HW+3 hours, spring tides. What's the stream?"

**Plugin Response**:
```
🌊 TIDAL DIAMOND LOOKUP

Diamond: F
Time: HW+3 hours
Tides: Springs

From Diamond F Table:
HW+3 Springs: 245°T at 2.8 knots

📊 RESULT:
SET: 245°T (WSW)
DRIFT: 2.8 knots

Application:
- Stream sets toward 245°T
- Vessel drifts 2.8 NM per hour in this direction
- Apply for ±1 hour either side of HW+3
- Use for EP and CTS calculations

Reference Port: [Chart indicates reference port]
Note: This is spring tide data - use directly for spring tides
```

### Example 5: Depth Safety Check
**User**: "Draught 1.8m, charted depth 3.2m, tide 2.1m CD. Am I safe with 0.5m UKC?"

**Plugin Response**:
```
🌊 DEPTH SAFETY CALCULATION

Vessel Requirements:
- Draught: 1.8m
- Desired UKC: 0.5m
- Required Depth: 1.8 + 0.5 = 2.3m

Available Depth:
- Charted Sounding: 3.2m
- Tide Height: 2.1m CD
- Available Depth: 3.2 + 2.1 = 5.3m

Safety Assessment:
Available (5.3m) > Required (2.3m)

✅ SAFE - Clearance: 3.0m

Actual UKC: 5.3 - 1.8 = 3.5m (well above minimum)

Notes:
- Chart Datum: LAT (UK standard)
- Add extra margin in rough seas
- Consider squat in shallow water at speed
```

### Example 6: Drying Height
**User**: "Drying height 1.2m, tide 2.5m, draught 1.5m, need 0.5m UKC. Can I pass?"

**Plugin Response**:
```
🌊 DRYING HEIGHT CALCULATION

Chart Shows: Drying 1.2m (above Chart Datum)
Current Tide: 2.5m CD

Step 1: Calculate Water Depth
Water Depth = Tide - Drying Height
            = 2.5 - 1.2
            = 1.3m

Step 2: Safety Check
Available Depth: 1.3m
Vessel Draught: 1.5m
Required Depth: 1.5 + 0.5 = 2.0m

Available (1.3m) < Required (2.0m)

⚠️ INSUFFICIENT DEPTH

Shortfall: 0.7m (need 0.7m more tide)

Recommendation:
Wait until tide reaches at least 2.7m CD
(Current: 2.5m, Need: +0.2m more)

Note: Drying heights are underlined on charts
```

### Example 7: Bridge Clearance
**User**: "Bridge 22m above HAT, tide +1.2m, mast 19.5m. Will I clear?"

**Plugin Response**:
```
🌊 VERTICAL CLEARANCE CHECK

Bridge Data:
- Charted Height: 22.0m above HAT
- Current Tide: +1.2m above HAT
- Available Clearance: 22.0 + 1.2 = 23.2m

Vessel:
- Mast Height: 19.5m

Safety Check:
Available (23.2m) > Required (19.5m)

✅ SAFE - Clearance: 3.7m

Notes:
- Tide ADDS to clearance (higher tide = safer)
- Charted heights above HAT (UK standard)
- Add margin for:
  • Heel when sailing
  • Swell/waves
  • Antennas on mast
  • Safety factor

Recommended: Maintain 2m minimum for comfort
Actual: 3.7m - GOOD clearance
```

## Special Cases & Warnings

### Irregular Tides
**Solent** (Southampton, Cowes, Portsmouth):
- Double high water
- Extended stand at HW
- Rule-of-twelfths unreliable
- MUST use specific tidal curve

**Poole Harbour**:
- Double high water
- Complex tidal patterns
- Use Poole-specific curves only

**Victoria BC (Canada)**:
- Mixed semi-diurnal tides
- Unequal HW/LW heights
- Complex tidal curves required

**Portland (Dorset)**:
- Tidal race off Portland Bill
- Streams can exceed 5 knots
- Critical timing for passage

### Safety Margins
**Minimum UKC**:
- Calm seas, power: 0.5m
- Calm seas, sail: 1.0m
- Rough seas: +0.5-1.0m
- Unknown seabed: +1.0m
- Rock/coral: +2.0m

**Squat Effect**:
- Vessel settles lower at speed in shallow water
- Add 0.2-0.5m to draught in channels
- Critical when depth < 2× draught

**Overhead Clearance Margins**:
- Minimum: 2.0m (calm)
- With swell: 3.0m
- Sailing (heel): 4.0m+
- Always err on side of caution

## Version History
- **v0.1.0** (2025-10-31): Initial plugin with 5 core skills (tide-calculator, tidal-diamond-reader, diamond-dispatcher, depth-datum-flipper, vertical-clearance-solver)
