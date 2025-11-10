# Estimated Position (EP) - Complete Worked Example

## Scenario
You're sailing from Plymouth to Fowey on a sunny day with moderate wind.

**Given Information**:
- Last visual fix: 09:30 at Eddystone Lighthouse (50°10.9'N, 004°15.9'W)
- Current time: 11:30 (2 hours elapsed)
- Course steered: 110°C
- Speed through water: 5.5 knots (log reading)
- Wind: Southwest Force 4, close-hauled on starboard tack
- Estimated leeway: 6° (moderate wind, close-hauled)
- Tidal stream (from chart diamond): Set 045°T, Drift 1.8 knots
- Compass deviation: 2°E
- Magnetic variation: 5°W (from chart)

**Question**: What is your Estimated Position at 11:30?

---

## SOLUTION

### STEP 1: DEAD RECKONING (DR)
*Calculate position using course and speed only*

**Convert Course to True**:
```
True = Compass + Deviation + Variation
True = 110°C + 2°E + (-5°W)
True = 110° + 2° - 5°
True = 107°T
```

**Calculate Distance Run**:
```
Time = 11:30 - 09:30 = 2 hours
Speed = 5.5 knots
Distance = Speed × Time = 5.5 × 2 = 11.0 nm
```

**Plot DR Position**:
- From fix at Eddystone: 50°10.9'N, 004°15.9'W
- Direction: 107°T
- Distance: 11.0 nm

**DR Position (11:30 DR)**: Approximately 50°05'N, 004°03'W
```
△ 11:30 DR – 50°05.0'N, 004°03.0'W
```

---

### STEP 2: APPLY LEEWAY
*Account for wind pushing vessel sideways*

**Leeway Direction**:
- Wind from: Southwest (225°)
- Vessel heading: 107°T (SE)
- Wind on: Starboard side
- Leeway direction: To leeward (northeast, starboard side)

**Apply Leeway**:
```
Wind on starboard → Add leeway to course
Water Track = Course Steered + Leeway
Water Track = 107°T + 6°
Water Track = 113°T
```

**Plot Water Track**:
- From fix at Eddystone
- Direction: 113°T (not 107°T)
- Distance: 11.0 nm (same as DR)

**Water Track Position**: Approximately 50°04.5'N, 004°02.0'W

---

### STEP 3: APPLY TIDAL STREAM
*Account for water movement carrying vessel*

**Tidal Vector**:
```
Set (direction): 045°T (NE)
Drift (speed): 1.8 knots
Time: 2 hours
Tidal Distance = 1.8 kts × 2 hrs = 3.6 nm
```

**Plot Tidal Stream**:
- From: Water Track Position (50°04.5'N, 004°02.0'W)
- Direction: 045°T
- Distance: 3.6 nm

**EP Calculation**:
- Start: Water track position
- Move: 045°T for 3.6 nm
- End: Estimated Position

---

### FINAL ANSWER

**ESTIMATED POSITION (EP) at 11:30**:
```
▽▽ 11:30 EP – 50°07.0'N, 003°58.5'W
```

---

## SUMMARY TABLE

| Position Type | Time | Latitude | Longitude | Notes |
|---------------|------|----------|-----------|-------|
| **Fix** ⊙ | 09:30 | 50°10.9'N | 004°15.9'W | Eddystone Lighthouse |
| **DR** △ | 11:30 | 50°05.0'N | 004°03.0'W | Course + Speed only |
| **Water Track** | 11:30 | 50°04.5'N | 004°02.0'W | DR + Leeway (intermediate) |
| **EP** ▽▽ | 11:30 | 50°07.0'N | 003°58.5'W | Water Track + Stream |

---

## VECTOR DIAGRAM

```
FIX (09:30)
⊙ Eddystone
50°10.9'N, 004°15.9'W
     │
     │ Course Steered: 107°T
     │ Speed: 5.5 kts
     │ Distance: 11.0 nm
     │
     ▼
DR (11:30)
△ 50°05.0'N, 004°03.0'W
     │
     │ Leeway Correction: +6° (starboard)
     │ Water Track: 113°T
     │ Distance: 11.0 nm (same)
     │
     ▼
WATER TRACK (11:30)
50°04.5'N, 004°02.0'W
     │
     │ Tidal Stream
     │ Set: 045°T (NE)
     │ Drift: 3.6 nm (1.8 kts × 2 hrs)
     │
     ▼
EP (11:30)
▽▽ 50°07.0'N, 003°58.5'W
```

---

## CONFIDENCE ASSESSMENT

**FIX QUALITY**: Visual fix on prominent lighthouse ✓ High confidence

**TIME ELAPSED**: 2 hours – ACCEPTABLE
- <1 hour: Excellent
- 1-3 hours: Good ✓ (We're here)
- 3-4 hours: Marginal
- >4 hours: Get new fix

**DATA QUALITY**:
- Course: Known from compass ✓
- Speed: From log (±10% typical) ✓
- Leeway: Estimated 6° (±2° typical) ⚠ Moderate confidence
- Stream: From chart diamond ✓ (±20% typical)

**OVERALL CONFIDENCE**: MEDIUM-HIGH

---

## VALIDATION CHECKS

### Check 1: Depth Sounder
```
EP Position: 50°07.0'N, 003°58.5'W
Chart depth (from chart): ~65m
Depth sounder reading: 62m
Tidal height above CD: +2.5m
Charted depth + tide = 65 + 2.5 = 67.5m

Actual depth: 62m
Expected depth: 67.5m
Difference: 5.5m (close enough ✓)
```
*Close match confirms EP is reasonable*

### Check 2: Visual Transit (if available)
Look for any visible transits or clearing bearings to validate position.

### Check 3: Distance Off
If you can take a bearing to visible object:
- Measure distance on chart
- Compare with radar range (if available)
- Should match EP distance

---

## RECOMMENDATIONS

✓ **Current EP is valid** for navigation (2 hours old, good confidence)

⚠ **Get new visual fix** within next 1-2 hours

⚠ **Before entering** confined waters, **MUST get new fix**

✓ **Monitor depth** sounder - should match chart + tide

✓ **Look for** visual transits or landmarks to validate

---

## PLOTTING NOTES

**On Chart**:
1. Mark Fix: ⊙ 09:30 at Eddystone
2. Draw course line: 107°T
3. Mark DR: △ 11:30 DR at 11 nm
4. Draw water track: 113°T (leeway applied)
5. From water track end, draw stream vector: 045°T, 3.6 nm
6. Mark EP: ▽▽ 11:30 EP at endpoint

**Pencil Technique**:
- Use soft pencil (2B) for easy erasing
- Label all positions with time
- Keep chart neat - erase old DR/EP when getting new fix

---

## WHAT HAPPENS NEXT?

**At 12:30** (1 hour later):
- Update EP from current EP (not from original fix)
- Or better: **Get new visual fix** if land visible
- EP is now 3 hours old from last fix - getting less reliable

**Best Practice**:
- Update EP every hour
- Get new fix every 2-3 hours
- Always get fix before entering hazards
- Never enter port on EP alone - need visual fix

---

## COMMON STUDENT ERRORS IN THIS EXAMPLE

❌ **Error 1**: Forgetting to apply leeway
- Wrong: Plot 11 nm at 107°T only (this is DR, not EP)
- Right: Plot at 113°T (includes leeway)

❌ **Error 2**: Leeway wrong direction (upwind instead of downwind)
- Wrong: 107°T - 6° = 101°T
- Right: 107°T + 6° = 113°T (wind on starboard, pushed to starboard)

❌ **Error 3**: Stream from wrong position
- Wrong: Plot stream from DR position
- Right: Plot stream from water track position (after leeway)

❌ **Error 4**: Wrong tidal drift distance
- Wrong: 1.8 nm (forgot to multiply by time)
- Right: 3.6 nm (1.8 kts × 2 hours)

❌ **Error 5**: Using old EP as "Fix"
- Wrong: Calling 11:30 EP a "fix" at 13:00
- Right: EP is always an estimate, not a fix

---

## KEY TAKEAWAYS

1. **EP = DR + Leeway + Stream** (always in that order)
2. **Leeway is DOWNWIND** (to leeward, starboard tack = add)
3. **Stream is plotted FROM water track endpoint**
4. **EP degrades with time** - get new fix regularly
5. **Validate with depth, transits, bearings** when possible
6. **Always label positions** with symbol and time
