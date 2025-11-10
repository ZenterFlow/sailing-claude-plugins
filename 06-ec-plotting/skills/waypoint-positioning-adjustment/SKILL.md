# Waypoint Positioning Adjustment for Safety

---
name: waypoint-positioning-adjustment
version: 1.0.0
triggers:
  - "waypoint offset"
  - "channel center waypoint"
  - "fog waypoint"
  - "depth contour navigation"
  - "waypoint positioning"
  - "safe waypoint placement"
---

## Purpose

Adjust waypoint positions from channel center to safer offset locations when navigating in restricted visibility to avoid collisions and maintain safe track. This skill reduces collision risk in fog by using strategic waypoint placement.

## Activation Triggers

This skill activates when you:
- Need to adjust waypoints for fog navigation
- Ask about channel-center waypoint safety
- Want to use depth contours for navigation
- Inquire about waypoint offsets in restricted visibility
- Need to set arrival alarms for offset waypoints

## Behavior

### Channel-Center Waypoints - The Problem

- **Mid-channel waypoint:** Directs vessel to center of channel
- **In fog:** Multiple vessels may navigate to same point
- **Collision risk:** Vessels converge on same location
- **Visibility:** Can't see other vessels until too close
- **Solution:** Offset waypoints to one side of channel

### Offset Strategy

**Choose safe side:** Usually port side (right-of-way implications)
**Use depth contour:** Follow 5m or 10m contour instead of center

**Advantages:**
- Vessels on opposite sides don't conflict
- One side usually clearer of traffic
- Depth contour provides additional guidance
- Maintains safe distance from both edges

### Depth Contour Navigation

**Select appropriate contour:** Based on vessel draught + clearance

**Example:** Draught 1.5m + 2m clearance = 3.5m minimum → use 5m contour

**Advantages:**
- Natural guide to destination
- Shows on radar overlay
- Depth alarm provides warning
- Follows safe water depth

### Waypoint Revision Steps

I'll guide you through this process:

1. Identify channel-center waypoint (e.g., WPT11 in middle)
2. Check chart for depth contours on safe side
3. Move waypoint to contour line (e.g., 5m contour)
4. Adjust arrival alarm for new location
5. Verify route clears all hazards
6. Test in good visibility first

### Arrival Alarm Considerations

- **Offset waypoint:** Alarm triggers when near contour, not channel center
- **Distance:** Set so alarm sounds with time to turn/observe
- **Typical:** 0.1-0.2 NM before waypoint
- **Purpose:** Alert that it's time to change course or look for next mark

### Common Errors to Avoid

❌ Keeping waypoints in channel center in fog
❌ Not using depth contours as guides
❌ Setting arrival alarm too close to waypoint
❌ Forgetting to check offset waypoint clears hazards

### Assessment Criteria

You should be able to:
- Revise 4 channel-center waypoints to safe offsets
- Select appropriate depth contour for vessel draught
- Explain why offset reduces collision risk
- Set arrival alarm distance for offset waypoint
- Demonstrate revised route checks clearance of hazards

---

**Version**: 1.0.0 (v0.8.0 - 2025-11-10)
