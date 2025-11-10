# Leeway Estimation Guide

## What is Leeway?
**Leeway** is the sideways drift of a vessel to leeward (downwind) due to wind pressure on hull and rigging.

**Direction**: ALWAYS downwind (to leeward)
**Magnitude**: Depends on:
- Wind strength
- Point of sail
- Hull shape
- Heel angle
- Sea state

## Leeway by Conditions

### Light Air (0-10 knots true wind)
| Point of Sail | Cruising Yacht | Racing Yacht | Motor-sailer |
|--------------|----------------|--------------|--------------|
| Close-hauled | 10-15° | 5-8° | 12-18° |
| Close reach | 8-12° | 4-6° | 10-14° |
| Beam reach | 5-8° | 3-4° | 6-10° |
| Broad reach | 2-4° | 1-2° | 3-5° |
| Running | 0-2° | 0-1° | 0-2° |

### Moderate Breeze (10-20 knots)
| Point of Sail | Cruising Yacht | Racing Yacht | Motor-sailer |
|--------------|----------------|--------------|--------------|
| Close-hauled | 5-10° | 3-5° | 8-12° |
| Close reach | 4-7° | 2-4° | 6-9° |
| Beam reach | 3-5° | 2-3° | 4-6° |
| Broad reach | 1-3° | 0-2° | 2-4° |
| Running | 0-1° | 0° | 0-2° |

### Fresh Wind (20-30 knots)
| Point of Sail | Cruising Yacht | Racing Yacht | Motor-sailer |
|--------------|----------------|--------------|--------------|
| Close-hauled | 3-7° | 2-4° | 5-8° |
| Close reach | 2-5° | 1-3° | 4-6° |
| Beam reach | 2-4° | 1-2° | 3-5° |
| Broad reach | 1-2° | 0-1° | 1-3° |
| Running | 0-1° | 0° | 0-2° |

### Strong Wind (30+ knots)
| Point of Sail | Cruising Yacht | Racing Yacht | Motor-sailer |
|--------------|----------------|--------------|--------------|
| Close-hauled | 2-5° | 1-3° | 4-6° |
| Close reach | 2-4° | 1-2° | 3-5° |
| Beam reach | 1-3° | 1-2° | 2-4° |
| Broad reach | 0-2° | 0-1° | 1-2° |
| Running | 0-1° | 0° | 0-1° |

## Why Leeway Decreases in Strong Winds
- Reefed sails = less windage
- More immersed hull = better grip
- Flatter boat (less heel) = better tracking
- Higher boat speed = better directional stability

## Special Situations

### Motor-Sailing
Reduce leeway by **50%** when engine is assisting:
- Example: Close-hauled in 15 knots normally 7°, motor-sailing: 3-4°

### Motor Only
Leeway is **negligible** (<1°) unless:
- Strong crosswind with large windage (high cabin, furled sails, davits)
- Very light displacement vessel
- Strong current/stream creating apparent wind

### Heavy Weather
Leeway **decreases** paradoxically:
- Reefed down = less sail area
- More hull in water = better grip
- Example: Force 8, deep-reefed: 2-3° vs Force 4 full sail: 5-7°

### Multihulls (Catamarans/Trimarans)
Significantly **less leeway** than monohulls:
- Wider beam = better lateral resistance
- Less heel = more efficient
- Typical: 50-70% of monohull leeway
- Example: Monohull 6°, catamaran 3-4°

## Which Way is Leeway Applied?

### Starboard Tack (wind from starboard/right)
- Vessel pushed to **PORT (left)**
- Leeway is **ADDED** to heading
- Example: Heading 090°T, leeway 5° → Water track 095°T

### Port Tack (wind from port/left)
- Vessel pushed to **STARBOARD (right)**
- Leeway is **SUBTRACTED** from heading
- Example: Heading 090°T, leeway 5° → Water track 085°T

### Easy Check
**Look downwind** - that's where leeway pushes you!

## Measuring Leeway (Advanced)

### Method 1: Trailing Line
- Stream light line astern
- Measure angle from centerline
- Angle = leeway

### Method 2: GPS Track vs Heading
- GPS Course Over Ground (COG) includes leeway
- Heading is from compass
- Difference = leeway + stream effect
- (Need to separate stream from leeway - requires stream data)

### Method 3: Wake Angle
- Look at wake pattern astern
- Wake angle from centerline ≈ leeway
- Works best in calm water

### Method 4: Experience/Tables
- Most Yachtmaster candidates use tables + experience
- Record leeway by conditions for your vessel
- Build personal leeway table

## Exam Expectations

**RYA Yachtmaster Offshore**:
- If not specified, assume: **5-7° for moderate conditions**
- Always state your assumption
- Show leeway on EP plot
- Explain direction (to leeward)

**Typical Exam Values**:
- Light: 10°
- Moderate: 5-7°
- Fresh: 3-5°
- Always applied downwind

## Common Errors

1. **Leeway upwind** ✗
   - Leeway is ALWAYS downwind (to leeward)

2. **Too much in strong winds** ✗
   - Remember: reefed sails = less leeway

3. **Forgetting point of sail** ✗
   - Close-hauled: maximum leeway
   - Running: minimal leeway

4. **Wrong sign** ✗
   - Starboard tack: add to heading
   - Port tack: subtract from heading

5. **Confusing with stream** ✗
   - Leeway: wind effect
   - Stream: water movement
   - Both applied separately in EP calculation

## Quick Reference Card

```
LEEWAY QUICK ESTIMATES
─────────────────────────────────────
Light air (cruising yacht):  10°
Moderate (cruising yacht):   5-7°
Fresh (cruising yacht):      3-5°

Direction: TO LEEWARD (downwind)

Starboard tack: ADD to heading
Port tack: SUBTRACT from heading

Running: negligible (~0°)
Close-hauled: maximum
Beam reach: moderate
```

## Related Skills
- See `ep-calculator` for full EP plotting
- See `cts-calculator` (Course to Steer) for pre-planning leeway
