---
name: time-zone-converter
description: Convert between Universal Time (UT), local zone times, and Daylight Saving Time using maritime designation systems.
license: CC-BY-SA
---

# SKILL: time-zone-converter
**RYA Yachtmaster – Maritime Time Zone Conversion**

## Purpose
Convert between Universal Time (UT/GMT), maritime time zones, and Daylight Saving Time for accurate tide table interpretation and tidal stream calculations. Essential for international navigation.

## Activation Triggers
- "time zone conversion"
- "UT to local time"
- "zone time"
- "DST conversion"
- "maritime time zones"
- "convert to GMT"
- "Zulu time"

## Behaviour
Convert times using maritime zone designations:

### Maritime Time Zone System

**Zone Designations:**
- **Z (Zulu)**: Universal Time (UT/GMT) - 0° longitude
- **A-M**: West of Greenwich (subtract hours from UT)
- **N-Y**: East of Greenwich (add hours to UT)
- Each zone = 15° longitude = 1 hour

**Common Zones:**
- Zone 0 (Z): UK, Portugal (UT/GMT)
- Zone -1 (N): Central Europe (UT-1)
- Zone -5 (R): US East Coast (UT-5)
- Zone +1 (A): West Atlantic (UT+1)
- Zone +8 (H): Singapore (UT+8)

### Conversion Rules

**UT → Zone Time:**
- Zone -1: UT - 1 hour (1200 UT = 1100 Zone -1)
- Zone +1: UT + 1 hour (1200 UT = 1300 Zone +1)

**Zone Time → UT:**
- Zone -1: Add 1 hour (1100 Zone -1 = 1200 UT)
- Zone +1: Subtract 1 hour (1300 Zone +1 = 1200 UT)

**Memory Aid**: "Zone number tells you how far from UT"
- Negative zone: West, behind UT (subtract from UT)
- Positive zone: East, ahead of UT (add to UT)

### Daylight Saving Time (DST)

**DST Rules:**
- Adds 1 hour to standard zone time
- Only active in specific months (check almanac)
- Almanac shows shaded/non-shaded periods
- NOT universal - varies by region

**Conversion Order:**
1. **Zone → UT**: Remove DST first, then convert zone
2. **UT → Zone**: Convert zone first, then add DST

**Examples:**
- Zone -1 DST → UT: Remove 1h (DST), add 1h (zone) = UT same as local
- UT → Zone -1 DST: Subtract 1h (zone), add 1h (DST) = UT same as local

## Example Output
```
MARITIME TIME ZONE CONVERSION
═══════════════════════════════════════

SCENARIO 1: UT to Zone -1 (No DST)
─────────────────────────────────────
Given: 1430 UT
Zone: -1 (Central Europe standard)

Conversion:
1430 UT - 1 hour = 1330 Zone -1

Result: 1330 Zone -1 ✓

═══════════════════════════════════════

SCENARIO 2: Zone -1 DST to UT
─────────────────────────────────────
Given: 1430 Zone -1 DST
Zone: -1 (Central Europe)
DST: Active (summer months)

Step 1: Remove DST
1430 - 1 hour = 1330 Zone -1 (standard)

Step 2: Convert to UT
1330 Zone -1 + 1 hour = 1430 UT

Result: 1430 UT ✓

Note: Zone -1 DST = UT (they match!)

═══════════════════════════════════════

SCENARIO 3: Complex Conversion
─────────────────────────────────────
Given: 0815 Zone +8 (Singapore)
Convert to: Zone -5 DST (US East Coast, summer)

Step 1: Convert to UT
0815 Zone +8 - 8 hours = 0015 UT

Step 2: Convert to Zone -5
0015 UT - 5 hours = 1915 Zone -5 (previous day)

Step 3: Add DST
1915 Zone -5 + 1 hour = 2015 Zone -5 DST

Result: 2015 Zone -5 DST (previous day) ✓

═══════════════════════════════════════

PRACTICAL APPLICATION: Tide Prediction
─────────────────────────────────────
Problem: Almanac shows HW at 1124 UT
Location: France (Zone -1 DST in summer)
Question: What time is HW in local time?

Solution:
1124 UT → Zone -1: 1124 - 1 = 1024 Zone -1
Add DST: 1024 + 1 = 1124 Zone -1 DST

Answer: HW is at 1124 local time (Zone -1 DST)

Note: In summer, Zone -1 DST = UT
      (the -1 and +1 cancel out)
```

## Time Notation

**24-hour format:**
- Always use 4 digits: 0815, 1430, 2245
- No colon typically: 1430 (not 14:30)
- Midnight: 0000, Noon: 1200

**Date changes:**
- 0015 UT on 16th is still 15th in Zone -5
- Always note date if crossing midnight
- Critical for multi-day passages

## Common Maritime Zones

| Zone | Designation | Offset | Example Location |
|------|-------------|--------|------------------|
| Z | Zulu | UT±0 | UK, Portugal, West Africa |
| N | November | UT-1 | Central Europe, West Med |
| O | Oscar | UT-2 | Mid-Atlantic |
| R | Romeo | UT-5 | US East Coast, Caribbean |
| S | Sierra | UT-6 | US Central |
| T | Tango | UT-7 | US Mountain |
| U | Uniform | UT-8 | US Pacific, Alaska |
| A | Alpha | UT+1 | West Atlantic |
| H | Hotel | UT+8 | Singapore, Hong Kong, Perth |
| K | Kilo | UT+10 | East Australia |
| M | Mike | UT+12 | New Zealand |

## DST Quick Reference

**Northern Hemisphere** (March-October/November):
- Europe: Last Sunday March → Last Sunday October
- US: 2nd Sunday March → 1st Sunday November

**Southern Hemisphere** (October-March/April):
- Australia: 1st Sunday October → 1st Sunday April
- New Zealand: Last Sunday September → 1st Sunday April

**Always check almanac** - dates vary by year and region!

## Common Errors to Avoid
- Adding when should subtract (and vice versa)
- Applying DST in wrong direction
- Forgetting DST only applies in specific months
- Not converting to UT as intermediate step
- Confusing ISO notation (UTC+1) with maritime (Zone -1)
- Using wrong date after midnight crossings

## Practical Tips
1. **Always convert through UT** - don't go directly between zones
2. **Check almanac shading** - shows DST active periods
3. **Write out steps** - reduces arithmetic errors
4. **Note date changes** - critical at midnight
5. **Verify with reality** - does the answer make sense?

## Version
v1.0.0 (2025-11-10)
