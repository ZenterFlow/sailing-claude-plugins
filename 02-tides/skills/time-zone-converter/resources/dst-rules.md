### Daylight Saving Time (DST) Rules for Navigation

#### What is DST?
Daylight Saving Time is a seasonal adjustment where clocks are advanced by 1 hour during warmer months to extend evening daylight. It is a **local/regional practice**, not universal.

#### Navigation Impact
- Tidal predictions in almanacs are published in **UT or standard zone time**
- When DST is active locally, you must convert almanac times to local DST time
- **Critical for safety**: Missing DST conversion = 1 hour error in tide times
- Always check almanac legend for time notation used

#### Common DST Regions

**Northern Hemisphere** (typically March/April to October/November):
- **UK**: British Summer Time (BST) = GMT + 1 = UT + 1
  - Last Sunday in March 01:00 UT → 02:00 BST
  - Last Sunday in October 01:00 UT → 01:00 GMT
- **Europe**: Central European Summer Time (CEST) = CET + 1
  - Last Sunday in March
  - Last Sunday in October
- **North America**: Varies by region
  - Second Sunday in March
  - First Sunday in November
  - Note: Arizona, Hawaii don't observe DST

**Southern Hemisphere** (typically October to March):
- **Australia**: AEST → AEDT (October to April)
- **New Zealand**: NZST → NZDT (September to April)
- Opposite to Northern Hemisphere seasons

**No DST Regions**:
- Most of Africa
- Most of Asia
- Equatorial regions
- Many island nations

#### Conversion Order (CRITICAL!)

**Converting TO UT** (from local time with DST):
```
Step 1: Remove DST (-1 hour)
Step 2: Apply zone conversion
```

**Converting FROM UT** (to local time with DST):
```
Step 1: Apply zone conversion
Step 2: Add DST (+1 hour)
```

**Why this order?**
- DST is applied to the **local zone time**, not to UT
- UT itself never observes DST
- DST is the "outermost" adjustment

#### Examples with Safety Notes

##### Example 1: Tidal Prediction Error
```
Almanac (UK): HW Portsmouth 1430 UT (June)
Local time BST: What time will HW occur?

Correct conversion:
1430 UT + 1 hour = 1530 BST

Incorrect (forgetting DST):
"HW is at 1430" ← WRONG! You'd be 1 hour early!
```

##### Example 2: Log Book Entry
```
Ship position: 15°W (Zone -1)
Date: 20 July (DST active)
Local ship time: 1645 Zone -1 DST

Converting to UT for log:
Step 1: Remove DST → 1545 Zone -1
Step 2: Zone -1 to UT (+1) → 1645 UT

Log entry: "1645 UT (1645 Zone -1 DST local)"
```

##### Example 3: Passage Planning
```
Departure: Falmouth (UK, BST active)
Arrival: Brest (France, CEST active)
HW Falmouth: 0700 UT
HW Brest: 0730 UT

What time on ship's clock (BST)?
Falmouth HW: 0700 UT + 1 = 0800 BST
Brest HW: 0730 UT + 2 = 0930 CEST

Plan departure for 0800 BST local time.
```

#### Checking DST Status

**In Almanacs**:
- Look for **shaded areas** on tidal graphs
- Legend will state: "Shaded areas indicate DST in effect"
- Time differences tables often note DST adjustments

**If Uncertain**:
- Always note date and location
- Check current almanac year (DST dates can change)
- When in doubt, use UT for all calculations (universal standard)

#### Common Errors to Avoid

1. **"BST is just UT renamed"** ✗
   - Wrong! BST = UT + 1

2. **"Add DST to UT"** ✗
   - Wrong! UT never has DST. DST is added to local zone time.

3. **"Same DST everywhere"** ✗
   - Wrong! DST is regional and varies by country/region.

4. **"Almanac times are in local time"** ✗
   - Usually wrong! Most almanacs use UT or standard zone time.
   - Always check almanac legend!

5. **"DST is 1 hour everywhere"** ✓
   - Actually correct! DST is always ±1 hour when used.

#### Safety Recommendation
**For navigation and log books**: Always record times in UT, then note local time in parentheses.

Example log entry:
```
1430 UT (1530 BST local)
Position: 50°12'N 004°08'W
HW Dover: 1642 UT (1742 BST)
```

This eliminates ambiguity and ensures accurate navigation.
