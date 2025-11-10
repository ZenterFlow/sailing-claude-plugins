### Daylight Saving Time (DST) Examples

**Critical Rule**: DST order matters!
- Converting TO UT: Remove DST FIRST, then apply zone
- Converting FROM UT: Apply zone FIRST, then add DST

#### Example 1: Understanding the Double Offset
```
Question: Why does Zone -1 DST equal UT?

Zone -1 DST = (UT - 1 hour) + 1 hour DST
            = UT - 1 + 1
            = UT

The zone offset and DST offset cancel each other out!

Example:
1430 Zone -1 DST = 1430 UT
```

#### Example 2: Zone +2 DST to UT
```
Given: 1620 Zone +2 DST
Find: UT

Step 1: Remove DST
1620 - 1 hour = 1520 Zone +2

Step 2: Convert Zone +2 to UT
Zone +2 = UT + 2, so UT = Zone +2 - 2
1520 - 2 hours = 1320 UT

Answer: 1620 Zone +2 DST = 1320 UT
(Total offset: -3 hours)
```

#### Example 3: UT to Zone -2 DST
```
Given: 0900 UT
Find: Zone -2 DST

Step 1: Convert to Zone -2
0900 UT - 2 hours = 0700 Zone -2

Step 2: Add DST
0700 + 1 hour = 0800 Zone -2 DST

Answer: 0900 UT = 0800 Zone -2 DST
(Total offset: -1 hour)
```

#### Example 4: BST vs Zone -1 DST
```
Both represent the same offset from UT:

BST = GMT + 1 hour = UT + 1 hour
Zone -1 DST = (UT - 1) + 1 = UT

Wait! These are different!

Correct understanding:
- BST is used for UK (which is Zone 0, not Zone -1)
- Zone 0 DST = UT + 1 hour = BST
- Zone -1 DST = UT (the offsets cancel)

So: 1200 UT = 1300 BST
    1200 UT = 1200 Zone -1 DST
```

#### Example 5: Date Line Considerations
```
Given: 2330 UT on 15 June
Find: Zone +12 on what date?

2330 UT + 12 hours = 1130 next day

Answer: 2330 UT (15 June) = 1130 Zone +12 (16 June)

WARNING: Date changes when crossing ±12 zones!
```

#### Common DST Periods (for reference)
- **UK/Europe**: Last Sunday March to last Sunday October
- **US/Canada**: Second Sunday March to first Sunday November
- **Southern Hemisphere**: Opposite to northern (e.g., Oct-Apr)

**Always check almanac shaded areas for active DST periods**
