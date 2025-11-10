# SKILL: Course to Steer Practical Integration

## Description
Execute a complete CTS solution from start to finish: plot position, determine tidal hour, construct vector triangle, apply all corrections, and calculate final compass course.

## Prerequisites
- SKILL_43-46 (All CTS component skills)
- SKILL_33 (Multi-Hour Tidal Integration)

## Learning Objectives
- Complete CTS workflow in under 10 minutes
- Integrate tidal streams, leeway, variation, and deviation
- Handle time zone and DST conversions
- Evaluate CTS quality (trip duration, tide strength)
- Adjust plan if CTS impractical (e.g., too much leeway)

## Complete Workflow
**Phase 1: Preparation (2 minutes)**
1. Plot start position accurately
2. Plot destination/waypoint
3. Draw ground track line
4. Measure ground track distance

**Phase 2: Tidal Analysis (2 minutes)**
5. Determine departure time and convert to reference port time
6. Calculate approximate trip duration (distance ÷ speed)
7. Select correct tidal hour offset from HW
8. Extract tidal direction and rate (diamond or atlas)
9. Apply computation of rates if between springs/neaps

**Phase 3: Vector Construction (3 minutes)**
10. Plot tidal vector FROM START POINT
11. Set dividers to boat speed (1 hour)
12. Arc to intersect ground track = intercept
13. Draw water track line
14. Measure True bearing (initial CTS)

**Phase 4: Corrections (2 minutes)**
15. Apply leeway (port/subtract, starboard/add)
16. Apply variation (west add, east subtract)
17. Look up deviation for magnetic course
18. Apply deviation (compass rules)
19. Final Compass Course for helmsman

**Phase 5: Verification (1 minute)**
20. Calculate actual trip duration
21. Verify tidal hour selection matches duration
22. Check leeway angle is reasonable
23. Note any warnings (strong cross-tide, long duration)

**Quality Checks:**
- CTS within 20° of ground track? (if not, check calculations)
- Trip duration reasonable? (if &gt;2 hours, consider re-planning)
- Leeway &lt;15°? (if more, consider different departure time)
- Tide not pushing you dangerously off track?

## Advanced Considerations
**Multi-Hour Trips:**
- Strongly consider plotting hourly tidal vectors
- CTS may need to be recalculated each hour
- Use integrated tide method (SKILL_33) for EP tracking

**Wind Against Tide:**
- Check if ground track crosses wind-over-tide zones
- May need to adjust departure time or waypoint
- Consider safety implications

**Practical Constraints:**
- If CTS requires impossible heading (e.g., into shallows), choose different departure time
- If tide too strong for boat speed, wait for slack water
- If leeway excessive, consider motoring or different sail plan

## Common Errors
- Rushing and skipping steps
- Applying corrections out of sequence
- Forgetting time zone conversions
- Not verifying intercept point location
- Accepting impractical CTS without question

## Assessment
- Complete 3 full CTS scenarios in &lt;30 minutes total
- Achieve final compass course within ±2° of correct answer
- Correctly handle multi-hour tide selection
- Identify when CTS is impractical and suggest alternatives
- Explain each step of workflow without reference