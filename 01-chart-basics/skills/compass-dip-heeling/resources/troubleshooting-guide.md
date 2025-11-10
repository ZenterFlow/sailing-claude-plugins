# Compass Dip and Heeling Error Troubleshooting Guide

## Diagnostic Decision Tree

```
START: Compass problem identified
│
├─ Problem Type?
│  │
│  ├─ SLUGGISH RESPONSE
│  │  └─ Go to Section 1: Sluggish Compass Diagnosis
│  │
│  ├─ INCONSISTENT HEADINGS (between tacks)
│  │  └─ Go to Section 2: Heeling Error Diagnosis
│  │
│  ├─ GPS DISCREPANCY (when heeled)
│  │  └─ Go to Section 2: Heeling Error Diagnosis
│  │
│  ├─ PLANNING HEMISPHERE CHANGE
│  │  └─ Go to Section 3: Compass Compatibility Check
│  │
│  └─ GENERAL ACCURACY CONCERNS
│     └─ Go to Section 4: Comprehensive Compass Check
```

---

## Section 1: Sluggish Compass Diagnosis

### Symptoms
- [ ] Compass card slow to settle after turn
- [ ] Card takes >5-10 seconds to stabilize
- [ ] Erratic or "sticky" movement
- [ ] Card appears to drag
- [ ] Reduced sensitivity to small course changes
- [ ] Card sits at angle (not level)

### Diagnostic Questions

**Question 1: Has vessel changed hemisphere or latitude zone recently?**

- **YES** → Likely dip imbalance (go to 1A)
- **NO** → Other causes likely (go to 1B)

---

### 1A: Dip Imbalance Investigation

**Check compass marking:**
```
Look for labels on compass:
□ "NH" or "Northern Hemisphere"
□ "SH" or "Southern Hemisphere"
□ "Zone 1" through "Zone 5"
□ "Global" or "Universal"
□ Latitude range (e.g., "30°N-60°N")
□ No marking visible
```

**Check current vessel location:**
```
Current latitude: _____________
Current hemisphere: North / South
Current zone requirement: _____________
```

**Compatibility check:**
```
Compass marked for: _____________
Currently sailing in: _____________

Compatible? YES / NO

If NO → Dip imbalance CONFIRMED
If YES → Dip imbalance unlikely (go to 1B)
```

---

**Dip Imbalance Severity Assessment:**

| Compass Zone | Current Location | Severity | Symptoms |
|--------------|------------------|----------|----------|
| Zone 2 (NH) | Zone 2 (NH) | None ✓ | Normal operation |
| Zone 2 (NH) | Zone 3 (Equat) | Mild ○ | Slightly sluggish |
| Zone 2 (NH) | Zone 4 (SH) | Severe ✗✗ | Very sluggish, unreliable |
| Zone 4 (SH) | Zone 4 (SH) | None ✓ | Normal operation |
| Zone 4 (SH) | Zone 3 (Equat) | Mild ○ | Slightly sluggish |
| Zone 4 (SH) | Zone 2 (NH) | Severe ✗✗ | Very sluggish, unreliable |
| Zone 3 (Equat) | Any | None-Mild ○ | Works acceptably anywhere |

---

**Action Required for Dip Imbalance:**

**Immediate (temporary):**
- Accept reduced accuracy
- Take bearings carefully, allow card to fully settle
- Cross-check with GPS whenever possible
- Avoid critical navigation in confined waters if possible
- Consider hand-bearing compass as backup
- Budget for compass replacement

**Short-term (days to weeks):**
- Source correct zone compass
  - If in foreign port: check local chandleries
  - If remote: order online with shipping to next port
  - Check manufacturer/model availability
- Plan installation
  - Check mounting compatibility
  - Electrical connections (if lit compass)
  - Professional installation if needed
- Budget: £150-400 for zone-specific, £400-800 for global

**Long-term (permanent fix):**
- Replace compass with correct zone
- If world cruising: consider global compass
- Swing new compass for deviation
- Test thoroughly before critical passage
- Update vessel documentation
- Dispose of old compass properly

---

### 1B: Other Causes of Sluggish Compass

**Mechanical Issues:**

**1. Pivot Wear/Damage**
```
Symptoms:
- Card drags or binds
- Irregular movement
- Card tilts to one side
- Scraping sound

Check:
- Age of compass (>10-15 years?)
- History of rough use or impacts
- Card freely suspended?

Action:
- Professional inspection
- Likely requires compass replacement
- Pivots rarely repairable
```

**2. Air Bubble in Compass Fluid**
```
Symptoms:
- Visible bubble in compass bowl
- Card movement sluggish
- Card may tilt
- Recent temperature changes?

Check:
- Inspect compass bowl for air bubble
- Check for fluid leaks (salt deposits around seal)
- Fluid level low?

Action:
- Small bubble (<5mm): acceptable, monitor
- Large bubble: requires refilling
- Fluid leak: seal damage, likely replacement needed
- Professional service recommended
```

**3. Card Rubbing on Bowl**
```
Symptoms:
- Scraping or dragging sensation
- Card uneven (warped)
- Damage to card visible
- Card tilts when compass level

Check:
- View card from side (level compass)
- Card centered in bowl?
- Card warped or bent?
- Bowl deformed?

Action:
- If card warped: replacement needed
- If bowl deformed: replacement needed
- Cannot be repaired
```

**4. Magnetization of Compass Card**
```
Symptoms:
- Sluggish on certain headings only
- Fast on other headings
- Inconsistent behavior
- Recent lightning strike or electrical fault?

Check:
- Does sluggishness vary with heading?
- Recent electrical/lightning event?
- Near strong magnetic field recently?

Action:
- Demagnetization sometimes possible
- Usually requires replacement
- Professional assessment needed
```

**5. Contaminated Fluid**
```
Symptoms:
- Cloudy or discolored fluid
- Sediment visible
- Very old compass (>20 years)
- Card movement dampened

Check:
- Fluid appearance (should be clear)
- Age of compass
- Any leaks or contamination entry

Action:
- Fluid replacement possible but expensive
- Often more cost-effective to replace compass
- Professional service required
```

---

## Section 2: Heeling Error Diagnosis

### Symptoms
- [ ] Compass readings differ on port vs. starboard tack
- [ ] GPS ground track differs from compass heading (beyond leeway)
- [ ] Compass inaccurate when vessel heeled
- [ ] Accurate when upright, inaccurate when heeled
- [ ] Error magnitude increases with heel angle

### Diagnostic Tests

**Test 1: Tack-to-Tack Comparison**

**Procedure:**
1. Sail close-hauled on port tack, steady wind
2. Record compass heading: _______°
3. Tack to starboard, maintain same trim/wind angle
4. Record compass heading: _______°
5. Calculate difference: _______°

**Expected results (no heeling error):**
- Difference should be ~90-110° (depending on tack angles)
- Example: Port tack 045°, Starboard tack 135° = 90° difference ✓

**Results indicating heeling error:**
```
Port tack:      045°
Starboard tack: 142°
Difference:     97° (should be ~90°)
→ 7° discrepancy indicates heeling error present
```

**Severity:**
```
Discrepancy < 3°:   Minor heeling error (acceptable)
Discrepancy 3-5°:   Moderate heeling error (monitor)
Discrepancy 5-10°:  Significant heeling error (mitigate)
Discrepancy > 10°:  Severe heeling error (act immediately)
```

---

**Test 2: GPS Cross-Check**

**Procedure:**
1. Sail on steady heading while heeled
2. Record compass heading: _______°
3. Record GPS ground track: _______°
4. Estimate leeway for conditions: _______°
5. Calculate expected GPS track:
   ```
   Compass heading: _______°
   Minus leeway:    _______°
   Expected GPS:    _______°
   Actual GPS:      _______°
   Discrepancy:     _______°
   ```

**Leeway estimates:**
```
Conditions           Typical Leeway
─────────────────────────────────
Close-hauled, light:      3-5°
Close-hauled, moderate:   5-8°
Close-hauled, heavy:      8-12°
Reaching:                 2-4°
Running:                  0-2°
```

**Interpretation:**
```
Discrepancy < 3°:   Compass accurate or leeway estimate good
Discrepancy 3-5°:   Minor heeling error or leeway misestimated
Discrepancy > 5°:   Likely heeling error present
```

---

**Test 3: Upright vs. Heeled Comparison**

**Procedure:**
1. Motor on compass heading 090° upright
2. Check GPS track: should be ~090° (minus current)
3. Sail same heading heeled 20°
4. Check GPS track: note difference
5. Difference = heeling error component

**Example:**
```
Upright:  Compass 090°, GPS 090° → Accurate ✓
Heeled:   Compass 090°, GPS 083° → 7° heeling error
```

---

### Heeling Error Magnitude Assessment

**Factors affecting magnitude:**

1. **Heel Angle:**
   ```
   5°:     Negligible (<1-2°)
   10°:    Minor (2-3°)
   15°:    Moderate (3-5°)
   20°:    Significant (5-8°)
   25°:    Serious (7-10°)
   30°+:   Severe (10-15°+)
   ```

2. **Latitude (Dip Angle):**
   ```
   Higher latitude (stronger dip):  Larger heeling error
   Lower latitude (weaker dip):     Smaller heeling error

   Example at 20° heel:
   - At 60°N: ~8° heeling error
   - At 40°N: ~6° heeling error
   - At 10°N: ~3° heeling error
   ```

3. **Compass Type:**
   ```
   Flat-mounted compass:    Maximum heeling error
   Gimballed compass:       Reduced heeling error (30-50% less)
   Gimballed + stabilized:  Minimal heeling error
   ```

4. **Heading:**
   ```
   Heeling error varies with heading:
   - Some headings: maximum error
   - Other headings: minimum error
   - Not easily predicted
   - Cannot be systematically corrected
   ```

---

### Action Required for Heeling Error

**Decision Matrix:**

| Heel Angle | Navigation Type | Action Required |
|------------|-----------------|-----------------|
| 0-10° | Any | None (negligible) |
| 10-15° | Open water | Monitor only |
| 10-15° | Confined water | GPS cross-check |
| 15-20° | Open water | GPS cross-check |
| 15-20° | Confined water | Reduce heel or GPS primary |
| 20-30° | Any | Reduce heel if critical nav |
| 20-30° | Confined water | GPS primary, add safety margin |
| >30° | Any | Reduce heel urgently, GPS only |

---

**Mitigation Strategies:**

**1. Reduce Heel (Most Effective)**
```
How:
- Ease sheets 15-20%
- Reef earlier
- Slow down temporarily
- Accept speed loss

When:
- Critical bearings
- Channel navigation
- Harbor approaches
- Collision avoidance bearings

Result:
- 25° → 15° heel reduces error by 50-70%
- Brief speed loss acceptable for accuracy
```

**2. GPS Cross-Check**
```
How:
- Note compass heading
- Check GPS ground track
- Account for leeway
- Use GPS for primary navigation

When:
- Cannot reduce heel
- Extended period heeled
- Open water navigation
- Position fixing

Result:
- Accurate navigation maintained
- Compass used for steering only
- Heading corrections based on GPS
```

**3. Hand-Bearing Compass (Held Level)**
```
How:
- Use hand-bearing compass
- Hold level (not tilted with vessel)
- Take bearings for position fix

When:
- Position fixing needed
- Collision avoidance bearings
- Critical navigation

Result:
- Eliminates heeling error
- Accurate bearings regardless of heel
- Requires practice in rough conditions
```

**4. Add Safety Margins**
```
How:
- Wider berth to hazards
- Conservative navigation
- Earlier course changes
- Position fixes more frequent

When:
- Cannot mitigate heeling error
- Confined waters navigation
- Poor conditions

Result:
- Compensates for compass uncertainty
- Reduces risk despite errors
```

---

## Section 3: Compass Compatibility Check

### Planning Hemisphere Change

**Scenario:** Relocating vessel or planning long passage

**Step 1: Identify Current Compass**
```
Check compass for markings:
Zone: _____________
Hemisphere: _____________
Latitude range: _____________
Manufacturer/Model: _____________
```

**Step 2: Identify Destination Requirements**
```
Destination: _____________
Latitude: _____________
Hemisphere: North / South
Zone required: _____________
```

**Step 3: Compatibility Assessment**

Use this table:

| Current Zone | Destination Zone | Compatible? | Action |
|--------------|------------------|-------------|--------|
| Zone 1-2 (NH) | Zone 1-2 (NH) | Yes ✓ | None required |
| Zone 1-2 (NH) | Zone 3 (Equat) | Marginal ○ | Will work, slightly degraded |
| Zone 1-2 (NH) | Zone 4-5 (SH) | NO ✗ | Must replace compass |
| Zone 4-5 (SH) | Zone 4-5 (SH) | Yes ✓ | None required |
| Zone 4-5 (SH) | Zone 3 (Equat) | Marginal ○ | Will work, slightly degraded |
| Zone 4-5 (SH) | Zone 1-2 (NH) | NO ✗ | Must replace compass |
| Zone 3 (Equat) | Any | Yes ✓ | Works acceptably everywhere |
| Global | Any | Yes ✓ | Works everywhere |

---

**Step 4: Plan Compass Acquisition**

**If replacement needed:**

**Option 1: Replace before departure**
```
Pros:
- Test new compass in familiar waters
- No rush
- Can swing compass properly
- Familiar with new compass before passage

Cons:
- May not find compass in current location
- Need to plan ahead

Timeline: 2-4 weeks before departure
```

**Option 2: Replace at destination**
```
Pros:
- Get correct zone compass where it will be used
- Local chandleries familiar with requirement
- No need to carry spare

Cons:
- Compass unreliable during passage
- May be difficult in remote location
- Delays at destination

Timeline: Upon arrival, before local sailing
```

**Option 3: Carry spare, install mid-voyage**
```
Pros:
- Flexibility
- Switch at optimal time (e.g., equator crossing)
- No delay at destination

Cons:
- Need to carry spare compass
- Installation at sea (challenging)
- Need installation hardware

Timeline: Switch when crossing into opposite hemisphere
```

**Option 4: Install global compass before departure**
```
Pros:
- Works everywhere
- No switching needed
- Future-proof for any sailing

Cons:
- Expensive (£400-800)
- May be harder to source
- Slightly less accurate than zone-specific

Timeline: 4-6 weeks before departure (allow ordering time)
```

---

### Equator Crossing Planning

**For passages crossing magnetic equator:**

**Route assessment:**
```
Start location: _____________ (Zone ___)
End location: _____________ (Zone ___)
Crosses equator? Yes / No
Hemisphere change? Yes / No
```

**Compass strategy:**

**If staying within Zone 3 range (20°S-30°N):**
- Zone 3 or Global compass works throughout ✓
- No compass change needed

**If crossing from NH to SH (e.g., Panama to New Zealand):**
- NH compass fails in SH
- Options:
  1. Global compass (works entire route)
  2. Switch compass at equator (carry spare)
  3. Rely on GPS, replace at destination

**If crossing from SH to NH (e.g., Australia to Mediterranean):**
- SH compass fails in NH
- Same options as above

**Recommended:** Install global compass before departure for any equator-crossing passage

---

## Section 4: Comprehensive Compass Check

### Annual Compass Health Check

**Perform annually or after any significant event (grounding, lightning, etc.)**

**Visual Inspection:**
```
□ Compass bowl clear (no cracks, leaks)
□ Fluid clear (not cloudy or discolored)
□ No air bubble or small bubble (<5mm)
□ Card freely moving (no sticking)
□ Card level when compass level
□ Card not warped or damaged
□ Markings legible
□ Night lighting functional (if fitted)
□ Mounting secure
□ Visible from helm
```

**Functional Tests:**
```
□ Card settles quickly after disturbance (< 5 seconds)
□ Card responds smoothly to vessel turn
□ No dead zones (card moves throughout 360°)
□ Repeatable readings (same heading = same reading)
□ Consistent with hand-bearing compass
□ Consistent with GPS heading
```

**Zone/Hemisphere Verification:**
```
□ Compass marked with zone/hemisphere
□ Zone appropriate for sailing area
□ If planning travel: compatibility checked
```

**Deviation Check:**
```
□ Deviation table exists and current
□ Deviation table < 3 years old
□ Significant metal/electrical changes since last swing? No
□ Deviation checked on at least 4 headings
□ Maximum deviation acceptable (<10°)
```

**Heeling Error Awareness:**
```
□ Understand heeling error concepts
□ Tested tack-to-tack readings if sailing vessel
□ Mitigation strategies known
□ GPS cross-check procedures established
```

---

### When to Replace Compass

**Definite replacement needed:**
- ✗ Wrong hemisphere/zone for sailing area
- ✗ Pivot damage (card drags, irregular movement)
- ✗ Fluid leak (loss of fluid, salt deposits)
- ✗ Card warped or damaged
- ✗ Large air bubble (>10mm)
- ✗ Bowl cracked or damaged
- ✗ Age >20 years

**Consider replacement:**
- ○ Small air bubble (5-10mm) and old compass
- ○ Sluggish movement (no obvious cause)
- ○ Difficult to read (faded markings)
- ○ Mounting obsolete or problematic
- ○ Planning hemisphere change (wrong zone)

**Monitor/service:**
- △ Small bubble (<5mm)
- △ Slight sluggishness (still functional)
- △ Night lighting failed (if otherwise OK)

---

## Quick Reference: Problem → Solution

```
PROBLEM                           LIKELY CAUSE              ACTION
────────────────────────────────────────────────────────────────────
Sluggish, recently sailed         Dip imbalance            Replace with
opposite hemisphere                                        correct zone

Sluggish, old compass              Pivot wear               Replace compass

Different readings on tacks        Heeling error            Reduce heel or
                                                           use GPS

GPS shows different heading       Heeling error or         Check heeling,
(when heeled)                     deviation                 cross-check

Air bubble visible                Leak or temperature      Small: monitor
                                                           Large: replace

Card scrapes or binds             Warped card or           Replace compass
                                  damaged pivot

Planning equator crossing         Wrong zone for           Install global
                                  destination               or carry spare

Inconsistent readings             Deviation or             Swing compass,
                                  magnetic interference     check interference

Night light not working           Bulb/LED failure         Replace bulb or
                                                           compass

Planning hemisphere move          Compass incompatible     Source new compass
                                                           before departure
```

---

## Professional Help

**When to consult professional:**
- Compass swing (deviation table creation)
- Fluid refill
- Electrical troubleshooting (lit compass)
- Installation of new compass
- Heeling error assessment (if complex)
- Demagnetization (rare)

**When DIY acceptable:**
- Visual inspection
- Functional testing
- GPS cross-checking
- Dip/zone compatibility check
- Hand-bearing compass deviation testing
- Replacement (if mechanically simple mount)

**Cost expectations:**
- Compass swing: £50-150
- Fluid refill: £100-200 (often not cost-effective)
- New compass (zone-specific): £150-400
- New compass (global): £400-800
- Installation labor: £50-150

---

## Documentation

**Keep records:**
```
Compass Log:
- Purchase date: _______________
- Manufacturer/Model: _______________
- Serial number: _______________
- Zone/Hemisphere: _______________
- Last deviation swing: _______________
- Deviation table location: _______________
- Service history: _______________
- Replacement planned: _______________
```

**Annual check record:**
```
Date: _______________
Inspector: _______________
Results: Pass / Concerns / Fail
Issues noted: _______________
Action taken: _______________
Next check due: _______________
```
