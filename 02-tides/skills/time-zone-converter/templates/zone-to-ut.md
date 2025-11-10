### Zone Time to UT Conversion Template

**Rule**: To convert zone time TO UT, work in reverse of the zone offset.

#### Example 1: Zone -1 to UT (no DST)
```
Given: 1200 Zone -1
Find: UT

Zone -1 means: local time = UT - 1 hour
Therefore: UT = local time + 1 hour

1200 Zone -1 + 1 hour = 1300 UT

Answer: 1200 Zone -1 = 1300 UT
```

#### Example 2: Zone +2 to UT (no DST)
```
Given: 1445 Zone +2
Find: UT

Zone +2 means: local time = UT + 2 hours
Therefore: UT = local time - 2 hours

1445 Zone +2 - 2 hours = 1245 UT

Answer: 1445 Zone +2 = 1245 UT
```

#### Example 3: Zone -1 DST to UT
```
Given: 1430 Zone -1 DST
Find: UT

Step 1: Remove DST (always first when going TO UT)
1430 - 1 hour = 1330 Zone -1

Step 2: Convert Zone -1 to UT
Zone -1 = UT - 1, so UT = Zone -1 + 1
1330 + 1 hour = 1430 UT

Answer: 1430 Zone -1 DST = 1430 UT

Note: The two 1-hour offsets cancel out!
```

#### Memory Aid
- **Zone -1**: "West is best" → ADD to get UT
- **Zone +1**: "East is least" → SUBTRACT to get UT
- **DST**: Always remove FIRST when converting TO UT
