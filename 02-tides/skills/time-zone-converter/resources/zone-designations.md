### Maritime Time Zone Designations (NATO/Admiralty System)

#### Zone Letter System
Each zone represents 15° of longitude (1 hour of time difference from UT).

| Letter | Zone | Offset from UT | Longitude Band | Example Location |
|--------|------|----------------|----------------|------------------|
| Z | 0 | ±0 hours | 7.5°W to 7.5°E | UK (GMT), West Africa |
| A | -1 | -1 hour | 7.5°W to 22.5°W | Azores, Cape Verde |
| B | -2 | -2 hours | 22.5°W to 37.5°W | Mid-Atlantic |
| C | -3 | -3 hours | 37.5°W to 52.5°W | Brazil, Argentina |
| D | -4 | -4 hours | 52.5°W to 67.5°W | Atlantic Canada, Caribbean |
| E | -5 | -5 hours | 67.5°W to 82.5°W | US East Coast, Colombia |
| F | -6 | -6 hours | 82.5°W to 97.5°W | US Central, Mexico |
| G | -7 | -7 hours | 97.5°W to 112.5°W | US Mountain |
| H | -8 | -8 hours | 112.5°W to 127.5°W | US Pacific, Alaska |
| I | -9 | -9 hours | 127.5°W to 142.5°W | Alaska |
| K | -10 | -10 hours | 142.5°W to 157.5°W | Hawaii, Aleutians |
| L | -11 | -11 hours | 157.5°W to 172.5°W | Samoa |
| M | -12 | -12 hours | 172.5°W to 180°W | Date Line West |
| N | +1 | +1 hour | 7.5°E to 22.5°E | France, Spain, Norway |
| O | +2 | +2 hours | 22.5°E to 37.5°E | Greece, South Africa |
| P | +3 | +3 hours | 37.5°E to 52.5°E | East Africa, Moscow |
| Q | +4 | +4 hours | 52.5°E to 67.5°E | UAE, Seychelles |
| R | +5 | +5 hours | 67.5°E to 82.5°E | Pakistan, Maldives |
| S | +6 | +6 hours | 82.5°E to 97.5°E | Bangladesh, Sri Lanka |
| T | +7 | +7 hours | 97.5°E to 112.5°E | Thailand, Indonesia |
| U | +8 | +8 hours | 112.5°E to 127.5°E | China, Singapore, Philippines |
| V | +9 | +9 hours | 127.5°E to 142.5°E | Japan, Korea |
| W | +10 | +10 hours | 142.5°E to 157.5°E | Australia East |
| X | +11 | +11 hours | 157.5°E to 172.5°E | Solomon Islands |
| Y | +12 | +12 hours | 172.5°E to 180°E | Date Line East, New Zealand |

**Note**: Letter J is omitted to avoid confusion with I.

#### Quick Conversion Rules

**From Zone Time TO UT:**
- **Negative zones (West)**: ADD the zone number
  - Zone -1: add 1 hour
  - Zone -5: add 5 hours
- **Positive zones (East)**: SUBTRACT the zone number
  - Zone +1: subtract 1 hour
  - Zone +8: subtract 8 hours

**From UT TO Zone Time:**
- **Negative zones (West)**: SUBTRACT the zone number
  - UT - 1 = Zone -1
  - UT - 5 = Zone -5
- **Positive zones (East)**: ADD the zone number
  - UT + 1 = Zone +1
  - UT + 8 = Zone +8

#### Memory Aids
- **West**: Negative numbers, "behind" UT
- **East**: Positive numbers, "ahead" of UT
- **Mnemonic**: "West is Best, East is Least" (when converting TO UT, add west, subtract east)
- **Z = Zulu = Zero = UT/GMT**

#### International Date Line
- Crosses through ±180° longitude
- Zone -12 (West side) and Zone +12 (East side) differ by 24 hours
- Crossing westbound: add 1 day
- Crossing eastbound: subtract 1 day

#### Standard vs Maritime Notation
- **Maritime**: Zone -1, Zone +2 (used in this skill)
- **ISO**: UTC-1, UTC+2 (used in aviation/computing)
- **Relationship**: They mean the same thing, just different notation
- **For sailing**: Always use maritime notation in log books and navigation
