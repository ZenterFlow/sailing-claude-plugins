### UT to Zone Time Conversion Template

**Rule**: To convert UT TO zone time, apply the zone offset directly.

#### Example 1: UT to Zone -1 (no DST)
```
Given: 1300 UT
Find: Zone -1

Zone -1 means: local time = UT - 1 hour

1300 UT - 1 hour = 1200 Zone -1

Answer: 1300 UT = 1200 Zone -1
```

#### Example 2: UT to Zone +3 (no DST)
```
Given: 0845 UT
Find: Zone +3

Zone +3 means: local time = UT + 3 hours

0845 UT + 3 hours = 1145 Zone +3

Answer: 0845 UT = 1145 Zone +3
```

#### Example 3: UT to Zone -1 DST (BST equivalent)
```
Given: 1200 UT
Find: Zone -1 DST

Step 1: Convert UT to Zone -1 (apply zone offset first)
1200 UT - 1 hour = 1100 Zone -1

Step 2: Add DST (always LAST when going FROM UT)
1100 + 1 hour DST = 1200 Zone -1 DST

Answer: 1200 UT = 1200 Zone -1 DST

Note: For UK waters, this is equivalent to BST
```

#### Example 4: UT to BST (British Summer Time)
```
Given: 0530 UT
Find: BST

BST = GMT + 1 hour = UT + 1 hour

0530 UT + 1 hour = 0630 BST

Answer: 0530 UT = 0630 BST
```

#### Memory Aid
- **Zone -1**: "Go west, lose an hour" → SUBTRACT from UT
- **Zone +1**: "Go east, gain an hour" → ADD to UT
- **DST**: Always add LAST when converting FROM UT
- **BST**: Simply add 1 hour to UT (DST is built into BST notation)
