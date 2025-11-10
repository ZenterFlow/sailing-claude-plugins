## Depth Calculation Examples

### Basic Depth Calculation Formula

```
Total Depth = Charted Depth + Height of Tide
```

Where:
- **Charted Depth**: Depth below CD (from chart, blue numbers)
- **Height of Tide**: Water level above CD at specific time (from tide tables)
- **Total Depth**: Actual water depth at that time

### Example 1: Simple Depth Calculation

**Scenario**: You want to anchor in a spot marked "8.5m" on the chart.

**Given**:
- Charted depth: 8.5m (below CD)
- Height of tide at 1400: 3.2m (above CD)
- Your draught: 2.0m
- Required under-keel clearance (UKC): 0.5m

**Calculation**:
```
Total depth = 8.5m + 3.2m = 11.7m

Under-keel clearance = Total depth - Draught
                     = 11.7m - 2.0m
                     = 9.7m UKC ✓ SAFE (well above 0.5m required)
```

### Example 2: Drying Height Calculation

**Scenario**: A rock with drying height "2.3" (underlined) on chart.

**Given**:
- Drying height: 2.3m (ABOVE CD, exposed at low water)
- Height of tide at 1030: 4.5m (above CD)
- Your draught: 1.8m
- Required UKC: 1.0m

**Calculation**:
```
Water depth over rock = Height of tide - Drying height
                      = 4.5m - 2.3m
                      = 2.2m

Under-keel clearance = Water depth - Draught
                     = 2.2m - 1.8m
                     = 0.4m UKC ✗ UNSAFE (less than 1.0m required)
```

**Decision**: Wait for higher tide or avoid the rock.

### Example 3: Minimum Tide Height Needed

**Scenario**: You need to cross a bar with drying height "1.7m".

**Given**:
- Drying height: 1.7m (above CD)
- Your draught: 2.2m
- Required UKC: 0.5m

**Question**: What minimum tide height do you need?

**Calculation**:
```
Required water depth = Draught + UKC
                     = 2.2m + 0.5m
                     = 2.7m

Minimum tide height = Drying height + Required water depth
                    = 1.7m + 2.7m
                    = 4.4m above CD

Answer: Wait until tide height reaches 4.4m or higher
```

### Example 4: Bridge Clearance

**Scenario**: Bridge shown as "25m" clearance (magenta) on chart.

**Given**:
- Charted clearance: 25m above HAT
- HAT: 7.0m above CD
- Current tide height: 5.2m above CD
- Your mast height: 18m above waterline

**Calculation**:
```
Actual clearance = Charted clearance + (HAT - Current tide)
                 = 25m + (7.0m - 5.2m)
                 = 25m + 1.8m
                 = 26.8m

Available clearance = 26.8m
Mast height        = 18.0m
Safety margin      = 8.8m ✓ SAFE
```

**Alternative** (if chart uses MHWS instead of HAT):
```
Charted clearance: 25m above MHWS
MHWS: 6.2m above CD
Current tide: 5.2m above CD

Actual clearance = 25m + (6.2m - 5.2m)
                 = 25m + 1.0m
                 = 26.0m ✓ Still SAFE
```

### Example 5: Maximum Draught for Passage

**Scenario**: Channel with charted depth "4.8m", crossing at low water springs.

**Given**:
- Charted depth: 4.8m (below CD)
- Tide height at MLWS: 0.8m (above CD)
- Required UKC: 0.5m

**Question**: What's the maximum draught that can safely pass?

**Calculation**:
```
Total depth = 4.8m + 0.8m = 5.6m

Maximum draught = Total depth - Required UKC
                = 5.6m - 0.5m
                = 5.1m

Answer: Vessels with draught up to 5.1m can pass at MLWS
```

### Example 6: Comparing Spring and Neap Conditions

**Scenario**: Shallow approach to harbor.

**Given**:
- Charted depth: 3.2m (below CD)
- MHWS: 5.4m above CD
- MHWN: 4.2m above CD
- Your draught: 2.5m
- Required UKC: 0.5m

**At Spring High Water**:
```
Total depth = 3.2m + 5.4m = 8.6m
UKC = 8.6m - 2.5m = 6.1m ✓ SAFE
```

**At Neap High Water**:
```
Total depth = 3.2m + 4.2m = 7.4m
UKC = 7.4m - 2.5m = 4.9m ✓ SAFE
```

**At Mean Low Water Springs (MLWS = 0.8m)**:
```
Total depth = 3.2m + 0.8m = 4.0m
UKC = 4.0m - 2.5m = 1.5m ✓ SAFE (just barely)
```

### Example 7: Light Visibility Height

**Scenario**: Lighthouse elevation "35m" on chart.

**Given**:
- Light elevation: 35m above MHWS
- MHWS: 5.8m above CD
- Your eye height: 3m above waterline
- Current tide: 2.5m above CD

**Calculation**:
```
Light height above CD = 35m + 5.8m = 40.8m

Water surface above CD = 2.5m

Light height above current sea level = 40.8m - 2.5m = 38.3m

Geographic range (approximate) = 2.08 × √(38.3) + 2.08 × √(3)
                                ≈ 12.9 + 3.6
                                ≈ 16.5 nautical miles
```

### Quick Reference Summary

| Situation | Formula |
|-----------|---------|
| **Total depth** | Charted depth + Height of tide |
| **Depth over drying height** | Height of tide - Drying height |
| **Under-keel clearance** | Total depth - Draught |
| **Bridge clearance** | Charted clearance + (HAT - Current tide) |
| **Required tide height** | Drying height + Draught + UKC |
| **Light height above sea** | Light elevation + MHWS - Current tide |

### Safety Checklist

Before any shallow water passage:
- [ ] Check charted depth or drying height
- [ ] Get current tide height from tables
- [ ] Calculate total depth
- [ ] Subtract draught
- [ ] Verify UKC meets requirements (0.5m power, 1.0m sail minimum)
- [ ] Add safety margin for swell and squat
- [ ] Check if area has irregular tidal pattern (Solent, Poole, etc.)
