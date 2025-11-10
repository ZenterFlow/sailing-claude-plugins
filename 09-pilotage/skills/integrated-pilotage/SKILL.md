# Integrated Pilotage Application

---
name: integrated-pilotage
version: 1.0.0
triggers:
  - "integrated pilotage"
  - "comprehensive pilotage"
  - "passage plan pilotage"
  - "complete pilotage"
  - "pilotage synthesis"
  - "end to end pilotage"
---

## Purpose

Synthesize all pilotage techniques into comprehensive passage plans, applying variation, tidal calculations, and multiple navigation aids for real-world scenarios.

## Activation Triggers

This skill activates when you ask about:
- Integrated or comprehensive pilotage
- Complete passage planning for pilotage
- Combining multiple pilotage techniques
- End-to-end pilotage plans
- Real-world pilotage application

## Behavior

### Comprehensive Planning Framework

**Part One - Open Water to Approach**:
- Starting waypoint: Exact coordinates (e.g., 46°10.89'N 006°15.15'W)
- Route segments: Logical legs with key waypoints
- Distance calculations: Overall and individual leg distances
- Speed selection: Appropriate boat speed (6kn/12kn/18kn)
- Tidal stream: Apply current effect to each leg
- Passage time: Calculate approximate duration
- ETA planning: Arrival time with contingency buffer

**Part Two - Harbor Pilotage to Mooring**:
- Visual verification at approach waypoint
- Buoyage navigation through harbor
- Final approach to moorings

### Tidal Height Integration

**HOT Reference**: Calculate Height of Tide for estimated arrival

**Contingency**: Subtract time buffer for early/late arrival

**Minimum Depths**: Add HOT to charted depths for each leg

**LW Check**: Verify depth at moorings on arrival and next Low Water

**Formula**: Safe Depth = Charted Depth + Height of Tide

### Visual Verification at Waypoints

**Buoy Identification**: Use specific buoy numbers and characteristics

**Back Bearings**: Plot on lights for safe passage between hazards

**Depth Confirmation**: Expected depth at each waypoint

**Turn Criteria**: Specific bearing or depth that triggers course change

**Example**: "At Green #3, depth 12m, turn to 060°(M) for next leg"

### Hazard Avoidance Strategies

Combine multiple techniques:

**Clearing Bearings**: For harbor entrances and narrow passages (NMT/NLT)

**Depth Contours**: Follow safe contour lines between hazards

**Leading Lines**: Use day/night transits for precise alignment

**Minimum Depths**: Establish safe depth limit for each leg

**Contingency Plans**: Alternative routes for each hazard area

### Standard Leg Format

**Each leg must specify**:

```
LEG [number]: [Leg name]
From: [Starting point]
To: [Ending point]
Course: [bearing]°(M) magnetic
Distance: [X.X] nautical miles
Min Safe Depth: [X]m + HOT
Expected Max Depth: [Y]m
Obstructions: [None / specific hazards]
Arrival Verification: [Bearing/depth check]
Action: [What to do at waypoint]
```

**Example**:
```
LEG 3: Entrance Channel
From: Green Buoy #3
To: East Cardinal Mark
Course: 277°(M)
Distance: 2.5 nm
Min Safe Depth: 5m + HOT = 7.3m (with 2.3m HOT)
Expected Max Depth: 35m
Obstructions: None
Arrival: Bearing to lighthouse 230°(M), depth ~8m
Action: Turn to 315°(M) for harbor entrance
```

### Night Departure from Anchorage

**Visual Aid Selection**:
- Leading lights: Identify if available for exit
- Clearing bearings: Use entrance lights for safe departure corridor
- Back bearings: Use astern bearings on lights to clear dangers
- Evaluate usefulness for different departure directions

**Contingency Options**:
- Multiple routes through hazard areas
- Determine if navigation aids usable for all directions
- Alternative marks if primary aid unavailable
- Safe abort points identified

### Plan Execution Discipline

**Cockpit Navigation**: Execute plan from cockpit, NOT below

**Hand Bearing Compass**: Primary monitoring tool for bearings

**Depth Sounder**: Continuous monitoring, especially near contours

**If Lost**: Stop near buoy, re-establish position before proceeding

**When in Doubt**: Stop vessel and fix position accurately

**Never**: Continue when uncertain - safety over schedule

### Documentation Standards

**Leg Numbering**: Clear sequential numbering (Leg 1, Leg 2, etc.)

**Magnetic Bearings**: All headings converted to magnetic (apply variation)

**Depth Reference**: Always include "+ HOT" notation for clarity

**Hazard Notes**: Specific warnings for each critical area

**Verification Points**: Clear criteria for each waypoint arrival

### Practical Example: Complete Harbor Entry

**Scenario**: Enter harbor from offshore waypoint to mooring

**Plan Components**:

```
PASSAGE: Offshore to Dawson Harbour Moorings
Variation: 6°W (apply to all bearings)
HOT at arrival: +2.3m (HW-2 hours)

LEG 1: Approach
From: Offshore waypoint (46°10.89'N 006°15.15'W)
Course: 045°(T) = 039°(M)
Distance: 5.5 nm
Pick up transit 277°(M) when visible
Min Depth: 20m + HOT, shoals to 8m near entrance

LEG 2: Transit Line
Course: 277°(M) (chimney and church spire aligned)
Distance: 1.2 nm
Min Depth: 5m + HOT = 7.3m
Stay on transit, monitor depth continuously

LEG 3: Harbor Entrance
Pass East Cardinal buoy to port
Course: 315°(M) after buoy
Distance: 0.8 nm
Center between Easterly and Southerly cardinals
Min Depth: 5m + HOT

LEG 4: Inner Harbor
Course: 000°(M)
Stay in deep channel between North and South cardinals
Min Depth: 5m + HOT
Marina entrance visible ahead

LEG 5: Final Approach
Course: Adjust as needed for mooring pickup
Verify depth > 6m with HOT
Southerly cardinal abeam to starboard
Visitors' moorings depth: 3m at chart datum = 5.3m with HOT

ARRIVAL CHECK:
- Current depth: 5.3m (adequate for 1.5m draft)
- Next LW: Check tide tables, verify 3m + LW HOT > 2m
- Holding: Good (chart notation)
```

### Common Errors to Avoid

❌ Failing to apply variation to all bearings consistently
❌ Not including Height of Tide in depth calculations
❌ Creating plans too detailed to follow on deck (overcomplicated)
❌ Omitting visual verification points for waypoints
❌ Neglecting contingency plans for restricted visibility
❌ Poor leg numbering or unclear course instructions
❌ Forgetting to monitor depth continuously near hazards
❌ Not integrating multiple techniques (using only one method)

### Assessment Criteria

You should be able to:
- Create complete passage plan from open water to mooring
- Apply variation correctly throughout entire plan
- Calculate tidal heights for arrival and next LW
- Integrate at least three different pilotage techniques in one plan
- Execute plan in simulation with proper cockpit discipline
- Create night departure plan with multiple route options
- Self-check plan against published standards

### Integration Examples

**Combining Techniques in One Plan**:
1. **Transit line**: For precise entrance alignment
2. **Clearing bearings**: To avoid rocks on both sides
3. **Depth contours**: As continuous safety check
4. **Leading lights**: For night precision
5. **GPS waypoints**: For position verification
6. **Hand bearing compass**: For all bearing checks

**Real-World Synthesis**:
- Plan created at chart table pre-departure
- Simplified for cockpit use
- All bearings magnetic
- All depths include HOT
- Multiple verification methods at each waypoint
- Contingency for every critical leg

---

**Version**: 1.0.0 (v1.1.0 - 2025-11-10)
