# Quick Reference: Compass Conversion Table

## Conversion Rules Summary

| From | To | Deviation | Variation | Direction |
|------|-----|-----------|-----------|-----------|
| **C** | **M** | Add E / Sub W | — | Apply Dev only |
| **M** | **T** | — | Add E / Sub W | Apply Var only |
| **C** | **T** | Add E / Sub W | Add E / Sub W | Apply both |
| **T** | **M** | — | Sub E / Add W | Reverse Var |
| **M** | **C** | Sub E / Add W | — | Reverse Dev |
| **T** | **C** | Sub E / Add W | Sub E / Add W | Reverse both |

---

## CADET Flow Chart

```
Going DOWN (C→T): Add East / Subtract West

    COMPASS (C)
        ↓
   [Deviation]
        ↓
   MAGNETIC (M)
        ↓
   [Variation]
        ↓
     TRUE (T)

Going UP (T→C): Add West / Subtract East
```

---

## Error Direction Quick Reference

### Easterly Errors
- **C → T**: ADD East
- **T → C**: SUBTRACT East

### Westerly Errors
- **C → T**: SUBTRACT West
- **T → C**: ADD West

---

## Common Exam Values (UK)

| Parameter | Typical Range | Example |
|-----------|---------------|---------|
| Variation (UK) | 0° to 10° W | 5°W |
| Deviation | 2° to 8° E/W | 3°E |
| Total Error | 5° to 15° | 8°W |

---

## Memory Aids

**CADET**
- **C**ompass
- **A**dd
- **D**eviation & **E**ast
- **T**rue

**"Error East, Compass Least"**
- When errors are East, Compass bearing is smaller than True

**"Can Dead Men Vote Twice"**
- **C**ompass
- **D**eviation
- **M**agnetic
- **V**ariation
- **T**rue

---

## Step-by-Step Checklist

### For C → T Conversion:
- [ ] Identify compass bearing
- [ ] Get deviation from table
- [ ] Apply deviation (Add E / Sub W) → Magnetic
- [ ] Get variation from chart
- [ ] Apply variation (Add E / Sub W) → True
- [ ] Check for wrap-around (>360° or <0°)
- [ ] Label answer (T)

### For T → C Conversion:
- [ ] Identify true bearing
- [ ] Get variation from chart
- [ ] Apply variation REVERSED (Add W / Sub E) → Magnetic
- [ ] Get deviation from table
- [ ] Apply deviation REVERSED (Add W / Sub E) → Compass
- [ ] Check for wrap-around
- [ ] Label answer (C)

---

## Error Troubleshooting

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Answer way off (>10°) | Added instead of subtracted | Reverse the operation |
| Bearing > 360° | Forgot to wrap | Subtract 360° |
| Bearing < 0° | Went negative | Add 360° |
| Lost track | No labels | Add (T)/(M)/(C) to each step |
| Inconsistent results | Wrong order | Dev first, then Var |

---

## Practice Pattern

1. Start simple: C→T with both errors East
2. Add complexity: Mix East and West
3. Practice reverse: T→C conversions
4. Handle edge cases: Wrap-around bearings
5. Speed drill: 10 conversions in 5 minutes
