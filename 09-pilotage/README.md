# Plugin 09: Pilotage

**Status**: ✅ Complete (13 skills implemented)

The Pilotage Tutor teaches comprehensive harbor navigation from fundamentals through advanced integrated techniques, including leading lines, clearing bearings, planning methods, and restricted visibility operations.

## Skills (13 total)

### Foundation (2 skills)
1. **pilotage-fundamentals** - Core concept of using visible objects to avoid invisible dangers, information sources
2. **chart-update-checker** - Verify charts are current and legal (SOLAS V requirement)

### Visual Navigation Techniques (3 skills)
3. **leading-lines-transit** - Charted transits, leading lights, lower light rule, compass deviation checks
4. **clearing-bearings** - NMT/NLT danger bearings for safe corridors between hazards
5. **moire-lights** - Precise bridge and entrance alignment using directional narrow-sector lights

### Planning and Execution (3 skills)
6. **pilotage-planning** - Create pictorial and rolling road plans for deck execution
7. **almanac-navigator** - Harbor entry notes and pilotage directions from almanacs
8. **harbor-entry-planner** - Comprehensive harbor approach plans with abort criteria

### Advanced Techniques (3 skills)
9. **restricted-visibility** - Fog pilotage using depth contours, radar, GPS with proper watchkeeping
10. **leading-line-plotter** - Transit range calculations and position fixing
11. **integrated-pilotage** - Synthesize all techniques into comprehensive passage plans

### Assessment (2 skills)
12. **clearing-bearing-calculator** - Calculate and verify clearing bearing corridors
13. **restricted-visibility-navigator** - COLREGS fog procedures and sound signals

## Installation

```bash
/plugin install pilotage@sailing-curriculum
```

## Usage Examples

### Pilotage Fundamentals
```
User: Why shouldn't I navigate from below using the chartplotter?

Agent: PILOTAGE PRINCIPLE - Visible objects avoid invisible dangers

       GPS shows WHERE you are, not WHAT is around you:
       • No hazard awareness from screen
       • Depth gauge confirms position
       • Visual features give continuous feedback
       • Crew safety requires skipper on deck

       Best Practice: Use GPS as ONE tool, not sole method.
       Navigator's place is COCKPIT during pilotage.
```

### Leading Lines and Lower Light Rule
```
User: Leading lights are misaligned - lower light is to the right. Which way do I turn?

Agent: LOWER LIGHT RULE - Always steer toward lower light

       Lower light RIGHT of upper → Turn RIGHT (starboard)

       This rule NEVER reverses (entering or leaving port).
       Make gentle turn to bring lights into vertical alignment.
```

### Clearing Bearings
```
User: Create clearing bearings for harbor entrance with rocks both sides

Agent: CLEARING BEARING SETUP

       Reference: Church spire ashore
       Left rocks clear at 212°(M) - label "NLT 212°(M)"
       Right rocks clear at 226°(M) - label "NMT 226°(M)"

       EXECUTION:
       • Keep bearing between 212° and 226°
       • At NMT limit (226°): Tack to starboard
       • At NLT limit (212°): Tack to port
       • Monitor depth as backup
```

### Pilotage Planning
```
User: Show me how to create a rolling road plan

Agent: ROLLING ROAD PLAN FORMAT

       Draw vertical line (vessel track)
       Start at bottom, work upward:

       ↑ MARINA (destination at top)
       LEG 3: 035°(M), 1.5nm, min 3m+HOT
       ↑ Red Buoy #4 (church bears 130°(M) abeam)
       LEG 2: 060°(M), 0.8nm, min 5m+HOT
       ↑ Green Buoy #3 (depth 12m)
       LEG 1: 045°(M), 1.2nm, min 8m+HOT
       ↑ ENTRANCE WAYPOINT (start at bottom)

       Compact, pocket-sized, sequential information.
```

### Restricted Visibility (Fog)
```
User: Fog just rolled in, visibility 0.5nm. What's my primary navigation tool?

Agent: PRIMARY TOOL IN FOG - Depth Contours

       • Follow safe depth contour lines
       • Add Height of Tide to charted depths
       • Continuous depth sounder monitoring
       • Most reliable when visual references lost

       BUOY LOCATION (10% Rule):
       Distance 2nm → Aim 0.2nm to one side
       At contour, turn toward buoy position

       COLREGS: Sound 1 long + 2 short every 2 min (sailing)
```

### Integrated Pilotage
```
User: Create complete passage plan from offshore to mooring

Agent: COMPREHENSIVE PILOTAGE PLAN
       Variation: 6°W | HOT at arrival: +2.3m

       LEG 1: Offshore Approach
       Course: 039°(M) | Dist: 5.5nm
       Pick up transit 277°(M) when visible
       Min depth: 20m+HOT

       LEG 2: Transit Line
       Course: 277°(M) (chimney/church aligned)
       Dist: 1.2nm | Min depth: 7.3m
       Stay on transit, monitor depth

       LEG 3: Harbor Entrance
       Pass E Cardinal to port → 315°(M)
       Clear between E and S cardinals
       Min depth: 7.3m

       LEG 4: Final Approach
       Moorings depth: 3m+2.3m HOT = 5.3m (adequate)
       Next LW check: Verify 3m + LW HOT > 2m
```

## Topics Covered

### Pilotage Fundamentals
- Core concept: visible objects to avoid invisible dangers
- Information sources (almanacs, pilot books, charts)
- Why GPS alone is insufficient for pilotage
- Cockpit vs below-deck navigation
- Variation application (True to Magnetic conversion)

### Visual Navigation Techniques
- Leading lines and charted transits (magenta lines)
- Leading lights operation and lower light rule
- Clearing bearings (NMT/NLT danger bearing corridors)
- Improvised transits from charted objects
- Compass deviation checks using known transits
- Moire lights for precise bridge/entrance alignment

### Planning Methods
- Pictorial/sketch plans (bird's eye view format)
- Rolling road plans (linear track format)
- Tram lines for channel navigation
- Required information checklist (tides, ports, visual aids, routes)
- Standard leg format (course, distance, depths, verifications)
- Chart protection (never take originals on deck)

### Execution Techniques
- Hand bearing compass continuous monitoring
- Depth contour navigation and following
- Tacking at clearing bearing limits
- Night pilotage with entrance lights
- Visual verification at each waypoint
- Height of Tide (HOT) calculations and application

### Restricted Visibility Operations
- Fog pilotage using depth contours (primary method)
- 10% circle of error rule for buoy location
- Radar and GPS as secondary navigation tools
- Proper watchkeeping discipline (all available means)
- COLREGS fog signals (Rule 35)
- Buoy search patterns on depth contours

### Integrated Application
- Comprehensive passage plans (open water to mooring)
- Multiple technique synthesis in single plan
- Tidal height integration throughout passage
- Hazard avoidance strategy combinations
- Contingency planning for all critical legs
- Night departures from anchorage with multiple routes
- Plan execution discipline (cockpit-based, when in doubt stop)

### Legal and Safety
- Chart currency requirements (SOLAS V Regulation 19)
- Port entry protocols and VHF communications
- Traffic separation scheme (TSS) navigation
- Emergency procedures (if lost, if uncertain)
- Abort criteria definition before approach

## Version
v1.1.0 (2025-11-10)
