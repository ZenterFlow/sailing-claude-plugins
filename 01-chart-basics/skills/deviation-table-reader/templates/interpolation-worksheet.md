# Deviation Interpolation Worksheet

## Given Information
- **Heading**: ___°M (or °C, check table type)
- **Table values**:
  - Lower bound: ___° = ___° (E/W)
  - Upper bound: ___° = ___° (E/W)

## Step 1: Calculate Fractional Position
```
Position = (Target - Lower) / (Upper - Lower)
         = (___° - ___°) / (___° - ___°)
         = ___ / ___
         = _____ (decimal fraction 0.0 to 1.0)
```

## Step 2: Calculate Deviation Range
```
Range = |Dev_Upper - Dev_Lower|
      = |___° - ___°|
      = ___°
```

## Step 3: Interpolate
```
Deviation = Dev_Lower + (Position × Range)
          = ___° + (_____ × ___°)
          = ___° + _____°
          = _____°
```

## Step 4: Round and Apply Direction
```
Rounded: ___° (E/W)

Special case check:
[ ] Crosses zero (E to W or W to E)?
    If yes: Result near 0°
```

## Step 5: Apply to Conversion
- **Compass → Magnetic**: Add East, Subtract West
- **Magnetic → Compass**: Subtract East, Add West

```
Example: 090°M with 6°E deviation
M → C: 090° - 6° = 084°C
```

## Quick Reference
**No interpolation needed if**:
- Exact match with table value, OR
- Within ±2° of table value, OR
- Deviation difference <1° between bounds
