# Angle Off Bow Position Fixing (45°/90° Method)

---
name: angle-off-bow-fix
version: 1.0.0
triggers:
  - "angle off bow"
  - "45 degree method"
  - "four point bearing"
  - "doubling the angle"
  - "distance off calculation"
  - "special angle fix"
---

## Purpose

Use relative bearings of 45° and 90° (or other special angles) to a charted object to determine distance off and approximate position without plotting bearing lines. This classic technique provides quick distance-off estimates when coastal cruising and is particularly useful for monitoring clearance from hazards.

## Activation Triggers

This skill activates when you:
- Ask about angle off bow methods
- Need quick distance off without full plotting
- Inquire about the "45-90 method" or "doubling the angle"
- Want special angle position techniques
- Need rapid coastal clearance checks

## Behavior

### The 45°/90° Method (Four Point Bearing)

**Core Principle:**
When an object moves from 45° relative to your bow to 90° relative (abeam), the distance you've traveled equals your distance off when abeam.

**Why It Works:**
- At 45°: You're on an isosceles right triangle
- At 90°: You're at the perpendicular
- Mathematical relationship: distance run = distance abeam

### Step-by-Step Method

**1. Setup (CRITICAL):**
- Maintain steady course (no course changes allowed)
- Identify prominent charted object ahead
- Prepare to note log readings and times
- Have stopwatch ready

**2. First Observation (45° Relative):**
- When object bears 45° relative to bow, note:
  - Log reading (or time + speed)
  - Course being steered
  - Time (if using speed calculations)
- Use hand bearing compass or relative bearing indicator
- **Do not change course after this point**

**3. Continue on Same Course:**
- Maintain exact same heading
- Monitor object moving aft along your side
- Prepare for second observation

**4. Second Observation (90° Relative - Abeam):**
- When object bears 90° relative (directly abeam), note:
  - Log reading (or time)
  - Confirm course unchanged

**5. Calculate Distance Off:**
```
Distance Off = Log₂ - Log₁

Example:
Log at 45°: 12.3 nm
Log at 90°: 14.2 nm
Distance Off = 14.2 - 12.3 = 1.9 nm
```

### Other Special Angles

**22.5°/45° Method (Doubling the Angle):**
- Distance run from 22.5° to 45° = distance off at 45°
- Useful for earlier warning

**26.5°/45° Method:**
- Distance run × 2 = distance off at 45°
- Allows more time between observations

**45°/90° Extended:**
- Most common and easiest to judge accurately

### Position Determination

Once you have distance off at 90°:
1. Plot your course line on chart
2. At 90° bearing moment, draw perpendicular from course line
3. Measure distance off along perpendicular
4. Mark position where perpendicular intersects 90° bearing line from object

### Limitations and Considerations

**Tidal Stream Effects:**
- Method assumes no tidal set (or negligible)
- Most accurate for short runs (<30 minutes)
- Combine with other fixes for tidal waters

**Course Accuracy:**
- Any course change invalidates the fix
- Helmsman must maintain steady heading
- Wind shifts requiring course adjustment = restart method

**Best Use Cases:**
- Monitoring distance offshore
- Estimating clearance from headlands
- Quick check when full plotting not needed
- Teaching bearing geometry to crew

**Not Suitable For:**
- Primary navigation in critical areas
- Situations requiring precise position
- When tidal streams are strong
- If course must change frequently

### Enhanced Accuracy

**Combine with Depth:**
- Cross-check distance off with charted depth
- Depth + tide should match charted depth at calculated position
- Significantly improves confidence

**Multiple Objects:**
- Use method on two different objects
- Provides cross-check
- Increases reliability

### Practical Examples

**Example 1: Coastal Passage**
```
Situation: Passing headland, need to know clearance
Object: Lighthouse on headland
Course: 090°T (steady)

At 45° relative (bearing 135° relative):
- Log: 23.4 nm

At 90° relative (bearing 180° relative):
- Log: 26.1 nm

Distance Off = 26.1 - 23.4 = 2.7 nm
Result: Clearing headland by 2.7 nm
```

**Example 2: Using Speed**
```
Situation: No log available, using SOG
Object: Church tower
Speed: 6.0 knots (steady)

At 45° relative:
- Time: 14:12

At 90° relative:
- Time: 14:38

Time elapsed = 26 minutes = 0.433 hours
Distance = 6.0 × 0.433 = 2.6 nm
Distance Off = 2.6 nm
```

### Common Errors to Avoid

❌ Changing course between observations (invalidates fix)
❌ Misidentifying exact 45° and 90° moments
❌ Using speed instead of distance run
❌ Forgetting tide effects in strong tidal areas
❌ Poor object identification (using wrong feature)

### Assessment Criteria

You should be able to:
- Execute angle method with <0.3 nm error compared to GPS
- Calculate distance off from given log readings in <30 seconds
- Explain why course must remain steady
- Assess when method is appropriate vs when full fix needed
- Identify special angle relationships (22.5/45, 26.5/45, 45/90)

---

**Version**: 1.0.0 (v0.9.0 - 2025-11-10)
