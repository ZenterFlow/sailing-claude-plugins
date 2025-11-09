# SKILL: Secondary Port Tidal Calculations

## Description
Calculate high/low water times and heights for secondary ports using standard port tide tables and correction data.

## Prerequisites
- SKILL_27 (Tide Tables)
- SKILL_28 (Tidal Curves)

## Learning Objectives
- Locate secondary port corrections in almanac
- Apply time differences for HW/LW based on standard port times
- Apply height corrections for MHWS/MHWN/MLWN/MLWS
- Interpolate corrections for intermediate times/heights
- Apply DST corrections AFTER secondary port calculations

## Correction Tables
**Time Corrections:**
- Standard port time ranges: 0000-0600, 0600-1200, 1200-1800, 1800-0000
- Find correction (mm) for each range
- Add to standard port HW/LW time

**Height Corrections:**
- **MHWS:** Correction applied to MHWS height at standard port
- **MHWN:** Correction applied to MHWN height
- **MLWN:** Correction applied to MLWN height
- **MLWS:** Correction applied to MLWS height
- Interpolate for intermediate heights

**DST Application Order:**
1. Convert local DST to UT (remove DST)
2. Perform secondary port calculations in UT
3. Convert result back to local time (add DST)

**Example:**
- Standard port: Dunbarton HW 0600 UT
- Secondary port correction: +002 (2 minutes)
- Secondary port HW = 0602 UT

## Common Errors
- Adding corrections before converting to UT
- Applying height corrections to wrong tidal level
- Not interpolating for intermediate tide heights
- Confusing time correction format (002 = 2 min, not 120 min)

## Assessment
- Calculate HW/LW times for 3 secondary ports with 100% accuracy
- Calculate heights for all four tidal levels
- Demonstrate correct DST application order