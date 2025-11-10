# Clearing Bearing Types: NMT vs NLT

## Visual Guide

```
         Reference Object (e.g., lighthouse)
                 │
                 │
    ─────────────┼─────────────
        SAFE     │    DANGER
       (LEFT)    │   (RIGHT)
                 │
            Hazard (rock)

NMT Rule: "No More Than XXX°"
→ Stay LEFT of bearing line (lower bearing numbers)
→ Safe: 000° to XXX°
→ Danger: XXX° + 1 to 360°
```

```
         Reference Object
                 │
                 │
    ─────────────┼─────────────
      DANGER     │    SAFE
      (LEFT)     │   (RIGHT)
                 │
            Hazard

NLT Rule: "No Less Than XXX°"
→ Stay RIGHT of bearing line (higher bearing numbers)
→ Danger: 000° to XXX° - 1
→ Safe: XXX° to 360°
```

## Quick Decision Guide

**Ask**: "Which side of the bearing line is safe water?"

- Safe water is to the LEFT (lower bearings) → Use **NMT**
- Safe water is to the RIGHT (higher bearings) → Use **NLT**

## Examples

### Example 1: NMT (No More Than)
- Hazard: Rock at 50°00'N, 005°00'W
- Reference: Lighthouse bearing 030°T from rock
- Passing: North of rock (safe water to north/left)
- Rule: **Keep bearing to lighthouse NMT 030°T**
- Safe zone: 000-030°T
- Danger zone: 031-360°T

### Example 2: NLT (No Less Than)
- Hazard: Shoal at 50°00'N, 005°00'W
- Reference: Headland bearing 270°T from shoal
- Passing: South of shoal (safe water to south/right)
- Rule: **Keep bearing to headland NLT 270°T**
- Danger zone: 000-269°T
- Safe zone: 270-360°T

## Memory Aid

**NMT**: "No **More** Than" = **Maximum** = Don't go **higher**
**NLT**: "No **Less** Than" = **Minimum** = Don't go **lower**

## Monitoring

Check clearing bearing every 5-10 minutes:

**If using NMT and bearing increases**:
- Getting closer to danger
- Turn to PORT (left) to reduce bearing

**If using NLT and bearing decreases**:
- Getting closer to danger
- Turn to STARBOARD (right) to increase bearing
