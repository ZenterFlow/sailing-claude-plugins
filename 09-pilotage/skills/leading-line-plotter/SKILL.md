---
name: leading-line-plotter
description: Calculate and plot leading lines (transits) for accurate position fixing and safe harbor entry navigation.
license: CC-BY-SA
---

# SKILL: leading-line-plotter
**RYA Yachtmaster – Leading Lines & Transits**

## Purpose
Calculate and use leading lines (transits) - two or more objects in line - for highly accurate position fixing and safe harbor entry. Leading lines provide instant position confirmation without compass errors and are the gold standard for pilotage accuracy.

## Activation Triggers
- "leading line"
- "transit"
- "leading marks"
- "objects in line"
- "range"
- "transit navigation"

## Behaviour
1. Identify transit objects (two charted objects that line up)
2. Calculate transit bearing from chart
3. Explain how to use for navigation:
   - **On the line**: Objects in line = vessel on transit bearing
   - **Left of line**: Rear object left of front = vessel left of transit
   - **Right of line**: Rear object right of front = vessel right of transit

4. Provide visual guidance and safety checks
5. Explain advantages: No compass error, instant position line, simple to use

## Example
User: "Church spire and water tower line up at 045°T on chart. How do I use this?"

Returns:
```
LEADING LINE (TRANSIT) GUIDANCE
═══════════════════════════════════════
Front object: Water tower
Rear object: Church spire
Transit bearing: 045°T

USAGE:
✓ When objects align: You are ON the 045°T line
→ Left of tower: You are LEFT (west) of line
→ Right of tower: You are RIGHT (east) of line

ADVANTAGES:
• No compass required (visual alignment)
• No variation/deviation errors
• Instant position fix
• Highly accurate (±10m typical)

MONITORING:
Check alignment every 1-2 minutes when using for approach
```

## Version
v1.0.0 (2025-11-09)
