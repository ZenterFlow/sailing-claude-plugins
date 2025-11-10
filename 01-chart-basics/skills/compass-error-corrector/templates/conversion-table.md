# Compass Error Conversion Quick Reference

## CADET Mnemonic (Compass → True)
```
C ompass
A dd
D eviation (if East)
E ast
T rue

Then: Add Variation (if East)
```

## Quick Conversion Table

### Compass → Magnetic → True
| Step | East Error | West Error |
|------|------------|------------|
| Apply Deviation (C→M) | ADD | SUBTRACT |
| Apply Variation (M→T) | ADD | SUBTRACT |

### True → Magnetic → Compass (Reverse)
| Step | East Error | West Error |
|------|------------|------------|
| Apply Variation (T→M) | SUBTRACT | ADD |
| Apply Deviation (M→C) | SUBTRACT | ADD |

## Memory Aids
- **"Error East, Compass Least"**: Compass reading is less than true bearing
- **"Error West, Compass Best"**: Compass reading is more than true bearing
- **CADET**: Always Compass to True direction
- **Reverse CADET**: Flip every add/subtract for True to Compass

## Worked Example Template
```
GIVEN:
Compass: ___°C
Deviation: ___° (E/W)
Variation: ___° (E/W)

STEP 1: C → M
___°C ± ___° (dev) = ___°M

STEP 2: M → T
___°M ± ___° (var) = ___°T

RESULT: ___°C = ___°T
```
