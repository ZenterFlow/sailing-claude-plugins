### Extreme Range Extrapolation Examples

#### Example 1: Range ABOVE MHWS (Very Large Spring)

**Scenario**: Exceptionally high spring tide

**Given Data**:
- Spring rate: 3.2 knots
- Neap rate: 1.6 knots
- Actual range: 7.2m
- MHWS: 6.5m, MHWN: 4.8m

**Analysis**: Range 7.2m > MHWS 6.5m → Extrapolation needed

**Calculation**:
```
Step 1: Calculate position factor
Range span = 6.5 - 4.8 = 1.7m
Position = (7.2 - 4.8) / 1.7
        = 2.4 / 1.7
        = 1.41

Position factor > 1.0 means range exceeds MHWS

Step 2: Interpolate (extrapolate) rate
Rate span = 3.2 - 1.6 = 1.6 knots
Adjustment = 1.6 × 1.41 = 2.26 knots
Interpolated rate = 1.6 + 2.26 = 3.86 knots

Step 3: Round
3.86 → 3.9 knots
```

**Answer**: 3.9 knots

**Graphical method**:
- Plot neap (1.6) and spring (3.2) points
- Draw interpolation line
- **Extend line beyond spring point** (to the right)
- Find 7.2m on range axis (beyond MHWS)
- Read up to extended line
- Read across to rate axis: ~3.9 knots

**Safety Note**:
⚠️ This is an extrapolation beyond published data. Rate may be greater than typical spring conditions. Cross-check with:
- Actual observed conditions
- More frequent position fixes
- Allow extra safety margin in passage plan

---

#### Example 2: Range BELOW MHWN (Very Small Neap)

**Scenario**: Exceptionally small neap tide

**Given Data**:
- Spring rate: 2.1 knots
- Neap rate: 0.9 knots
- Actual range: 2.8m
- MHWS: 5.2m, MHWN: 3.4m

**Analysis**: Range 2.8m < MHWN 3.4m → Extrapolation needed

**Calculation**:
```
Step 1: Calculate position factor
Range span = 5.2 - 3.4 = 1.8m
Position = (2.8 - 3.4) / 1.8
        = -0.6 / 1.8
        = -0.33

Negative position factor means range below MHWN

Step 2: Interpolate (extrapolate) rate
Rate span = 2.1 - 0.9 = 1.2 knots
Adjustment = 1.2 × (-0.33) = -0.40 knots
Interpolated rate = 0.9 + (-0.40) = 0.5 knots

Step 3: Round
0.5 knots (already at 0.1 precision)
```

**Answer**: 0.5 knots

**Graphical method**:
- Plot neap (0.9) and spring (2.1) points
- Draw interpolation line
- **Extend line beyond neap point** (to the left)
- Find 2.8m on range axis (below MHWN)
- Read up to extended line
- Read across to rate axis: ~0.5 knots

**Safety Note**:
⚠️ This is an extrapolation beyond published data. Rate may be weaker than typical neap conditions. This could mean:
- Slower progress against tide than expected
- Less tidal assistance when with tide
- Adjust passage timing accordingly

---

#### Example 3: Midpoint Range (Perfect Check)

**Scenario**: Range exactly halfway between neap and spring

**Given Data**:
- Spring rate: 3.0 knots
- Neap rate: 1.0 knots
- MHWS: 6.0m, MHWN: 4.0m
- Actual range: 5.0m (exactly midway)

**Calculation**:
```
Step 1: Position factor
Range span = 6.0 - 4.0 = 2.0m
Position = (5.0 - 4.0) / 2.0 = 1.0 / 2.0 = 0.5
(exactly 50% from neap to spring)

Step 2: Interpolate rate
Rate span = 3.0 - 1.0 = 2.0 knots
Adjustment = 2.0 × 0.5 = 1.0 knot
Interpolated rate = 1.0 + 1.0 = 2.0 knots
```

**Answer**: 2.0 knots

**Verification**: This is exactly the average of spring and neap rates:
- Average = (3.0 + 1.0) / 2 = 2.0 ✓

**Use this as a mental check**: If range is midway, rate should be average of spring and neap.

---

#### Quick Reference: Extrapolation Indicators

| Position Factor | Interpretation | Action |
|-----------------|----------------|--------|
| 0.0 | Exactly at neap | Use neap rate directly |
| 0.0 to 1.0 | Between neap and spring | Standard interpolation |
| 0.5 | Exactly midway | Rate = average of spring and neap |
| 1.0 | Exactly at spring | Use spring rate directly |
| > 1.0 | Above spring range | Extend line right, rate > spring |
| < 0.0 | Below neap range | Extend line left, rate < neap |

**General extrapolation caution**: Predictions become less reliable outside published ranges. Always verify with actual observations when possible.
