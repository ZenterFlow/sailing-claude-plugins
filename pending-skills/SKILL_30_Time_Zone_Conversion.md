# SKILL: Maritime Time Zone Conversion

## Description
Convert between Universal Time (UT), local zone times, and Daylight Saving Time using maritime designation systems.

## Prerequisites
- None (fundamental skill)

## Learning Objectives
- Identify maritime time zone designations (A-Z, ±hours)
- Convert UT to zone time and vice versa
- Apply DST corrections correctly
- Handle nested conversions (zone + DST)
- Use ISO vs maritime notation appropriately

## Conversion Rules
**Maritime Designations:**
- **Letters A-Z:** Each = 15° longitude (1 hour)
- **Z (Zulu):** UT/GMT
- **Zone -1:** UT - 1 hour = West of Greenwich
- **Zone +1:** UT + 1 hour = East of Greenwich

**DST Rules:**
- Add 1 hour to UT in non-shaded areas when active
- DST is LOCAL to region, not universal
- Remove DST first when converting to UT
- Add DST last when converting from UT

**Conversion Process:**
- **UT → Zone -1 DST:** UT → Zone -1 (subtract 1h) → Add DST (add 1h)
- **Zone -1 DST → UT:** Remove DST (subtract 1h) → Convert to UT (subtract 1h)
- **Total: Zone -1 DST = UT - 2 hours**

**Examples:**
- 1200 Zone -1 = 1100 UT
- 1200 Zone -1 DST = 1000 UT
- 1200 UT = 1300 Zone +1

## Common Errors
- Adding when should subtract (and vice versa)
- Forgetting DST is applied after zone conversion
- Confusing ISO offset notation with maritime zone notation
- Not checking almanac for DST active periods

## Assessment
- Convert 8 times between UT/zone/DST in &lt;3 minutes
- Explain conversion logic for Zone +2 DST to UT
- Identify correct DST application from almanac shading