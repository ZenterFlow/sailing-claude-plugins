# CADET Mnemonic Diagram

## The One-Way Rule

```
         COMPASS (C)
              ↓
         ADD EAST
              ↓
        MAGNETIC (M)
              ↓
         ADD EAST
              ↓
          TRUE (T)
```

**CADET = Compass Add East (to get) True**

---

## Full Conversion Flow

```
COMPASS → MAGNETIC → TRUE
   (C)        (M)       (T)
    |         |         |
    +----DEV----+       |
    |                   |
    +--------VAR--------+
```

**Going Down (C→T):** Add East / Subtract West
**Going Up (T→C):** Add West / Subtract East

---

## The Complete Picture

```
                TRUE NORTH
                    ↑
                    | True Bearing (T)
                    |
            [VARIATION]
            (geographic)
                    |
                    | Magnetic Bearing (M)
                    |
            [DEVIATION]
            (ship-specific)
                    |
                    | Compass Bearing (C)
                    ↑
              COMPASS CARD
```

---

## Quick Decision Tree

**START: What do I have?**

→ **Compass Bearing (C)?**
   - Add East Deviation → get Magnetic (M)
   - Add East Variation → get True (T)

→ **True Bearing (T)?**
   - Add West Variation → get Magnetic (M)
   - Add West Deviation → get Compass (C)

→ **Magnetic Bearing (M)?**
   - To get True: Add East Variation
   - To get Compass: Add West Deviation

---

## Error Direction Summary

| Error | Direction | C→M/T | T→M→C |
|-------|-----------|-------|--------|
| Deviation | East | **ADD** | **SUBTRACT** |
| Deviation | West | **SUBTRACT** | **ADD** |
| Variation | East | **ADD** | **SUBTRACT** |
| Variation | West | **SUBTRACT** | **ADD** |

---

## Memory Phrase

**"Cadets Are Magnificent Veterans True"**

- **C**ompass
- **A**dd
- **D**eviation = **M**agnetic
- **A**dd again
- **V**ariation = **T**rue

When going backwards (True → Compass), reverse everything!
