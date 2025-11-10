### Common Reference Ports for Tidal Stream Computations

When using tidal diamonds or atlas pages, each references a specific standard port for range calculations. Always verify which port to use.

#### UK & Ireland Reference Ports

| Reference Port | MHWS (m) | MHWN (m) | MLWN (m) | MLWS (m) | Typical Range | Areas Covered |
|----------------|----------|----------|----------|----------|---------------|---------------|
| **Dover** | 6.7 | 5.3 | 2.1 | 0.8 | 4.5 - 5.9 | Eastern Channel, Strait of Dover |
| **Portsmouth** | 4.7 | 3.8 | 1.9 | 0.8 | 3.0 - 3.9 | Solent, Isle of Wight |
| **Plymouth** | 5.5 | 4.4 | 2.2 | 0.8 | 3.6 - 4.7 | Western Channel, Devon/Cornwall |
| **Milford Haven** | 6.8 | 5.0 | 2.6 | 0.7 | 4.3 - 6.1 | Bristol Channel, South Wales |
| **Liverpool** | 9.3 | 7.4 | 3.2 | 1.2 | 6.2 - 8.1 | Irish Sea, North Wales |
| **Greenock** | 3.4 | 2.8 | 1.0 | 0.4 | 2.4 - 3.0 | Firth of Clyde, West Scotland |
| **Leith** | 5.6 | 4.4 | 2.4 | 1.1 | 3.3 - 4.5 | Firth of Forth, East Scotland |
| **Ullapool** | 4.9 | 3.7 | 2.2 | 0.9 | 2.8 - 4.0 | Northwest Scotland |
| **Stornoway** | 4.4 | 3.4 | 1.8 | 0.7 | 2.7 - 3.7 | Outer Hebrides |
| **Lerwick** | 1.6 | 1.2 | 0.6 | 0.2 | 1.0 - 1.4 | Shetland Islands |
| **Cobh** | 3.8 | 2.9 | 1.4 | 0.5 | 2.4 - 3.3 | South Ireland |
| **Galway** | 4.6 | 3.4 | 1.9 | 0.7 | 2.7 - 3.9 | West Ireland |

#### European Atlantic Coast

| Reference Port | MHWS (m) | MHWN (m) | Range | Areas Covered |
|----------------|----------|----------|-------|---------------|
| **Brest** | 7.5 | 5.9 | 5.9 - 7.5 | Brittany, Bay of Biscay north |
| **La Rochelle** | 6.2 | 4.9 | 4.9 - 6.2 | Bay of Biscay, West France |
| **Lisbon** | 3.8 | 2.9 | 2.9 - 3.8 | Portugal coast |
| **Vigo** | 3.5 | 2.6 | 2.6 - 3.5 | Northwest Spain |

#### Mediterranean

| Reference Port | MHWS (m) | MHWN (m) | Range | Notes |
|----------------|----------|----------|-------|-------|
| **Gibraltar** | 1.0 | 0.6 | 0.6 - 1.0 | Western Med entrance |
| **Valencia** | 0.3 | 0.2 | 0.2 - 0.3 | East Spain (minimal tides) |
| **Marseille** | 0.3 | 0.2 | 0.2 - 0.3 | South France (minimal tides) |

**Note**: Mediterranean has minimal tidal range, but significant currents exist.

#### North American East Coast

| Reference Port | MHWS (m) | MHWN (m) | Range | Areas Covered |
|----------------|----------|----------|-------|---------------|
| **Halifax** | 2.1 | 1.6 | 1.6 - 2.1 | Nova Scotia |
| **Saint John** | 8.2 | 6.5 | 6.5 - 8.2 | Bay of Fundy (extreme tides) |
| **Boston** | 3.0 | 2.4 | 2.4 - 3.0 | New England |
| **New York** | 1.5 | 1.2 | 1.2 - 1.5 | New York harbor |
| **Charleston** | 1.7 | 1.3 | 1.3 - 1.7 | Southeast US |

#### Caribbean

| Reference Port | MHWS (m) | MHWN (m) | Range | Notes |
|----------------|----------|----------|-------|-------|
| **Bermuda** | 0.9 | 0.7 | 0.7 - 0.9 | Mid-Atlantic |
| **San Juan** | 0.4 | 0.3 | 0.3 - 0.4 | Puerto Rico (minimal) |
| **Panama** | 3.5 | 2.8 | 2.8 - 3.5 | Caribbean side |

#### Pacific Examples

| Reference Port | MHWS (m) | MHWN (m) | Range | Areas Covered |
|----------------|----------|----------|-------|---------------|
| **San Francisco** | 2.1 | 1.5 | 1.5 - 2.1 | California coast |
| **Seattle** | 3.7 | 2.9 | 2.9 - 3.7 | Puget Sound |
| **Sydney** | 1.8 | 1.4 | 1.4 - 1.8 | East Australia |
| **Auckland** | 3.2 | 2.5 | 2.5 - 3.2 | New Zealand |

---

### How to Use This Information

#### Step 1: Identify Reference Port
Check the tidal diamond note or atlas header:
```
"Rates referred to HW Dover"
or
"Tidal streams are for Range at Plymouth"
```

#### Step 2: Get Current Range
Calculate range for that reference port:
```
Range = HW height - LW height
```

Use tidal prediction for the reference port, not your position.

#### Step 3: Apply to Computation Graph
Use the range from the reference port with spring/neap rates from your local tidal diamond or atlas.

---

### Common Mistakes

**Error 1: Using wrong reference port**
```
Wrong: "I'm near Portsmouth, so I'll use Portsmouth range"
If the diamond says "referred to HW Dover", you MUST use Dover range
```

**Error 2: Using range at your position**
```
Wrong: Calculating range where you are
Right: Range at the reference port specified by the diamond/atlas
```

**Error 3: Confusing reference ports**
```
Chart has multiple diamonds, each may reference different ports
Always check the specific diamond's reference notation
```

---

### Example Scenario

**Situation**:
- Position: Off Brighton (50°49'N, 000°07'W)
- Using: Tidal diamond "L" from Chart 1652
- Diamond note: "Rates referred to HW Dover"

**Correct procedure**:
1. Get today's HW/LW heights at **Dover** (not Brighton!)
2. Calculate range at Dover: e.g., HW 6.1m - LW 1.3m = 4.8m range
3. Read spring/neap rates from diamond L (for your position)
4. Use computation of rates graph with:
   - Dover range (4.8m)
   - Diamond L spring/neap rates
   - Dover MHWS/MHWN values (6.7m / 5.3m)

**Result**: Interpolated rate applies at diamond L position, based on Dover tidal range.

---

### Finding Reference Port Information

**In Almanacs**:
- Check atlas introduction page
- Look at diamond/atlas legend
- Often stated at top or bottom of each page

**On Charts**:
- Diamond boxes include reference notation
- Usually abbreviated: "HW Dov" = HW Dover
- Legend explains abbreviations

**If Uncertain**:
- Check almanac index for atlas section
- Read introduction to tidal stream predictions
- When in doubt, standard ports are usually the reference
- Can contact UKHO or almanac publisher for clarification

---

### Regional Variations

**Strong Tidal Areas** (>2m range):
- English Channel
- Bristol Channel
- Irish Sea
- Bay of Fundy
- More critical to get accurate interpolation

**Weak Tidal Areas** (<1m range):
- Mediterranean
- Caribbean
- Pacific Islands
- Less critical, but still important for current calculations

**Always verify the reference port for your specific chart or atlas page.**
