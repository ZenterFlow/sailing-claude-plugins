### Quick Mental Approximation Method

For rapid passage planning when precise calculation isn't critical, use mental shortcuts.

#### The "Thirds Rule" Approximation

**When range is:**
- **Near neap** (lower 1/3): Rate ≈ Neap + 1/4 of rate span
- **Middle** (middle 1/3): Rate ≈ Average of spring and neap
- **Near spring** (upper 1/3): Rate ≈ Spring - 1/4 of rate span

**Example**:
```
Spring: 3.0 knots, Neap: 1.5 knots
Rate span = 3.0 - 1.5 = 1.5 knots

Near neap: 1.5 + (1.5 ÷ 4) = 1.5 + 0.4 ≈ 1.9 knots
Middle: (3.0 + 1.5) ÷ 2 = 2.25 ≈ 2.3 knots
Near spring: 3.0 - (1.5 ÷ 4) = 3.0 - 0.4 ≈ 2.6 knots
```

**Accuracy**: Within ±0.2 knots typically, suitable for initial planning.

---

#### The "Range Percentage" Method

**Mental steps**:
1. Estimate where range falls as a percentage
2. Apply that percentage to rate span
3. Add to neap rate

**Example**:
```
Spring: 2.5 knots, Neap: 1.0 knots, Rate span: 1.5 knots
MHWS: 6.0m, MHWN: 4.0m, Range span: 2.0m
Actual range: 5.0m

Mental calculation:
"5.0 is 1.0 above 4.0, that's 50% of the 2.0 range span"
"50% of 1.5 knot rate span is 0.75 knots"
"1.0 neap + 0.75 = 1.75, call it 1.8 knots"

Answer: 1.8 knots (actual precise answer: 1.75, so very close!)
```

---

#### Pre-Calculated Rate Table

For frequently used locations, create a lookup table:

**Example**: Tidal Diamond "M", Reference Port: Dover

| Range (m) | Rate (knots) | Notes |
|-----------|--------------|-------|
| 3.5 (MHWN) | 1.2 | Neaps |
| 4.0 | 1.5 | Small neap |
| 4.5 | 1.8 | Below average |
| 5.0 | 2.0 | Average |
| 5.5 | 2.3 | Above average |
| 6.0 | 2.6 | Small spring |
| 6.5 (MHWS) | 2.8 | Springs |
| 7.0 | 3.1 | Very large spring |

**Usage**: Read directly or interpolate between table values.

**Creation**:
1. Use full computation method for 5-7 key ranges
2. Space evenly between MHWN and MHWS
3. Add one below and one above for extremes
4. Laminate and keep with chart

---

#### Quick Check: The "Sanity Test"

Before using any calculated rate, verify:

✓ **Result is between neap and spring** (unless extrapolating)
  - If not, check calculation order

✓ **Higher range = higher rate** (for normal conditions)
  - Spring rate should be greater than neap
  - If not, check you haven't swapped spring/neap

✓ **Precision is 0.1 knot**
  - Almanac rates are given to 0.1 knot
  - Your interpolation shouldn't be more precise

✓ **Rate seems reasonable for location**
  - English Channel: typically 0.5 - 4.0 knots
  - Open ocean: typically 0.1 - 1.0 knot
  - Narrow channels: can exceed 5.0 knots

---

#### Example: Quick Calculation Under Time Pressure

**Situation**: Approaching waypoint, need rate estimate NOW

**Data from almanac**:
- "3.5 springs, 1.7 neaps"
- Current conditions: "range about 4.5m, roughly mid-tide"

**Quick mental process**:
```
"Mid range means mid rate"
"Average of 3.5 and 1.7..."
"That's 3.5 + 1.7 = 5.2, divided by 2 = 2.6 knots"
"Use 2.6 knots for now, can refine later if needed"
```

**When time allows later**:
- Do full calculation with precise range value
- Adjust EP if significantly different
- Log both estimated and calculated rates

---

#### When NOT to Use Quick Methods

Avoid shortcuts when:
- **Narrow margins of safety** (e.g., crossing shallow bar)
- **Long passages** (errors accumulate over time)
- **Racing** (precision matters for performance)
- **Exam conditions** (show full working!)
- **Teaching/demonstrating** (don't teach shortcuts first)

**Best practice**: Learn the full method thoroughly first, then use shortcuts for routine planning only.

---

#### Verification Example

**Quick method result**: 2.3 knots
**Full calculation**: 2.28 knots → rounds to 2.3 knots

Difference: 0.0 knots ✓

**Over a 6-hour passage**:
- Difference in tidal effect: 0.0 NM
- This is acceptable for practical navigation

**Rule of thumb**: If quick method agrees with full calculation within ±0.2 knots, it's good enough for routine use.
