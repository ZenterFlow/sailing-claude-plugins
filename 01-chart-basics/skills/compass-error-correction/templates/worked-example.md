# Worked Examples: CADET Conversions

## Example 1: Compass → True (Classic CADET)

### Scenario
You take a compass bearing of **340°(C)** on a lighthouse. Your ship's deviation table shows **5°E** for headings around 340°, and the chart's compass rose shows variation is **10°W**.

What is the True bearing?

### Solution

```
COMPASS → TRUE (Add East)

Given Data:
- Compass bearing: 340°(C)
- Deviation: 5°E
- Variation: 10°W

Step 1: Compass → Magnetic (apply deviation)
  Deviation is EAST → ADD
  340°(C) + 5°E = 345°(M)

Step 2: Magnetic → True (apply variation)
  Variation is WEST → SUBTRACT
  345°(M) - 10°W = 335°(T)

✅ ANSWER: 335°(T)
```

**Check:** Started at 340°, ended at 335°. Deviation East made it bigger, Variation West made it smaller. ✓

---

## Example 2: True → Compass (Reverse CADET)

### Scenario
The chart shows a leading line on **085°(T)**. You need to steer this course on your ship's compass.

Given:
- Variation: 7°W
- Deviation: 3°E (for headings near 085°)

What compass course should you steer?

### Solution

```
TRUE → COMPASS (Reverse CADET)

Given Data:
- True bearing: 085°(T)
- Variation: 7°W
- Deviation: 3°E

Step 1: True → Magnetic (reverse variation)
  Variation is WEST → ADD (going backward)
  085°(T) + 7°W = 092°(M)

Step 2: Magnetic → Compass (reverse deviation)
  Deviation is EAST → SUBTRACT (going backward)
  092°(M) - 3°E = 089°(C)

✅ ANSWER: Steer 089°(C)
```

**Check:** True was 085°, Compass is 089°. "Error East, Compass Least" is backwards here (Compass is MORE), which confirms we added West and subtracted East correctly. ✓

---

## Example 3: Wrap-Around (359° → 362°)

### Scenario
Compass bearing: **358°(C)**
Deviation: **6°E**
Variation: **2°E**

Convert to True.

### Solution

```
COMPASS → TRUE

Step 1: Compass → Magnetic
  358°(C) + 6°E = 364°(M)
  Wrap-around: 364° - 360° = 004°(M)

Step 2: Magnetic → True
  004°(M) + 2°E = 006°(T)

✅ ANSWER: 006°(T)
```

**Key Point:** Always handle bearings > 360° by subtracting 360°.

---

## Example 4: Mixed Errors (East and West)

### Scenario
Compass: **120°(C)**
Deviation: **4°W**
Variation: **5°E**

Convert to True.

### Solution

```
Step 1: Compass → Magnetic
  Deviation is WEST → SUBTRACT
  120°(C) - 4°W = 116°(M)

Step 2: Magnetic → True
  Variation is EAST → ADD
  116°(M) + 5°E = 121°(T)

✅ ANSWER: 121°(T)
```

**Note:** Started at 120°, ended at 121°. The East variation (+5°) was slightly more than the West deviation (-4°), so net is +1°.

---

## Example 5: Magnetic → True (Partial Conversion)

### Scenario
You're given a magnetic bearing from an old chart: **270°(M)**
Current variation: **8°W**

Convert to True for plotting.

### Solution

```
MAGNETIC → TRUE (No deviation needed)

Given:
- Magnetic bearing: 270°(M)
- Variation: 8°W

Calculation:
  Variation is WEST → SUBTRACT
  270°(M) - 8°W = 262°(T)

✅ ANSWER: 262°(T)
```

**Note:** Only one step because we're starting from Magnetic (deviation already accounted for or not relevant).

---

## Summary Table

| Example | Start | Dev | Var | End | Method |
|---------|-------|-----|-----|-----|---------|
| 1 | 340°C | 5°E | 10°W | 335°T | C→M→T (CADET) |
| 2 | 085°T | 3°E | 7°W | 089°C | T→M→C (Reverse) |
| 3 | 358°C | 6°E | 2°E | 006°T | C→M→T (wrap) |
| 4 | 120°C | 4°W | 5°E | 121°T | C→M→T (mixed) |
| 5 | 270°M | — | 8°W | 262°T | M→T (partial) |
