# SKILL: GPS Data Interpretation (SOG, COG, XTE, TTG, VMG)

## Description
Interpret key GPS data fields, understand their relationship to log and compass data, and apply them for navigation decisions.

## Prerequisites
- SKILL_48 (GPS Fundamentals)
- Understanding of log and compass principles

## Learning Objectives
- Define SOG, COG, XTE, TTG, VMG
- Explain why SOG differs from log speed
- Use XTE for track monitoring and tacking decisions
- Interpret TTG for passage timing
- Apply VMG for sail trimming and routing optimization

## Data Field Definitions
**SOG (Speed Over Ground):**
- GPS-calculated speed using previous and current positions
- Includes effect of tide and leeway
- Formula: Distance between fixes ÷ time interval
- **Log speed:** Speed through water only (no tide/leeway)
- Example: Log 5 kn + 4 kn tide = SOG 9 kn

**COG (Course Over Ground):**
- GPS-calculated direction of movement over ground
- May differ from compass heading due to tide/leeway
- Derived from fix-to-fix positions

**XTE (Cross Track Error):**
- Lateral distance from planned ground track
- Displays direction: "Off to Port/Starboard" or arrow
- Used to monitor deviation and trigger tacking
- Can set alarm limits (e.g., 0.5 miles for safety)

**TTG (Time To Go):**
- Time to waypoint at current SOG
- Formula: Distance ÷ speed × 60 (minutes)
- Assumes constant SOG

**VMG (Velocity Made Good):**
- Speed directly toward destination waypoint
- Useful when tacking or not on direct course
- Accounts for zigzag path efficiency

## Common Errors
- Confusing SOG with log speed
- Ignoring XTE until too large
- Not understanding TTG assumes constant speed
- Forgetting COG can differ from heading

## Assessment
- Given log speed and tide, calculate expected SOG
- Interpret XTE display and determine corrective action
- Explain when VMG is more useful than SOG
- Set appropriate XTE alarm for narrow channel
- Calculate TTG from distance and SOG