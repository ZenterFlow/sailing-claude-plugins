# Bearing Geometry Guide

## Ideal Bearing Angles

### Three-Point Fix
- **Ideal**: All bearings 60° apart (creates equilateral triangle)
- **Good**: 40-80° separation
- **Acceptable**: 30-150° separation
- **Poor**: <30° or >150° separation

### Two-Point Fix
- **Ideal**: 90° between bearings (right angle)
- **Good**: 60-120° separation
- **Acceptable**: 45-135° separation
- **Poor**: <45° or >135° separation

## Why Geometry Matters

### Shallow Cut (<30° or >150°)
- Small position line error → LARGE position error
- Intersection point very uncertain
- Avoid if possible

### Good Cut (60-90°)
- Small position line error → Small position error
- Precise intersection
- Most reliable fix

## Visual Guide
```
GOOD GEOMETRY (60° apart)         POOR GEOMETRY (<30° apart)
        N                                 N
        ↑                                 ↑
       60°                               20°
    ←----→                            ←--→
   /      \                          /    \
  /   ✓    \                        /  ✗   \
 /          \                      /        \
Object A    Object B        Object A    Object B

Cocked hat: SMALL               Cocked hat: LARGE
Fix: RELIABLE                   Fix: UNRELIABLE
```

## Position Line Error Sources
1. **Compass error**: ±2-5° typical
2. **Bearing measurement**: ±1-3° (hand-bearing compass)
3. **Object identification**: Ensure correct charted object
4. **Timing**: Take all bearings within 30 seconds

## Cocked Hat Interpretation

### Size Assessment
- **<0.1 nm (200m)**: Excellent - perfect for pilotage
- **0.1-0.3 nm (200-600m)**: Good - suitable for coastal navigation
- **0.3-0.5 nm (600m-1km)**: Acceptable - use with caution
- **>0.5 nm (>1km)**: Poor - re-take bearings immediately

### Shape Analysis
- **Equilateral triangle**: All bearings equally reliable
- **Long thin triangle**: One bearing unreliable (discard it)
- **No triangle (lines don't meet)**: Systematic error - check deviation, variation, or object ID

## Best Object Selection
1. **Close objects** better than distant (bearing changes faster)
2. **Well-defined** (lighthouse > church tower > headland)
3. **Good spread** around vessel (not all in one sector)
4. **Prominent charted** objects (verify on chart first)

## Quick Fix Quality Check
1. Plot reciprocals from objects
2. Check if they form small cocked hat
3. If cocked hat >0.5 nm: one bearing is likely wrong
4. If no cocked hat forms: systematic error (deviation/variation wrong)

## When to Retake Bearings
- Cocked hat >0.5 nm
- One bearing clearly off (long skinny triangle)
- Uncertain of object identification
- Entering restricted waters or hazards nearby
- Fix is >10 minutes old
