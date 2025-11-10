# SKILL: Running Fix (Transferred Position Line)

## Description
Plot a running fix using a single charted object by transferring the first bearing line using DR and tidal vectors to intersect with a second bearing.

## Prerequisites
- Dead reckoning plotting (SKILL_34)
- Bearing conversion (SKILL_21)

## Learning Objectives
- Take and plot initial bearing to single object
- Transfer first bearing line using DR distance and tide
- Plot second bearing and determine fix position
- Explain why initial bearing line position is arbitrary
- Assess fix accuracy compared to circle of error

## Step-by-Step Method
**Step 1:** Take first bearing of object, convert to True, plot line from object seaward. Note time/log.

**Step 2:** Choose ANY point on bearing line as assumed position (arbitrary).

**Step 3:** Plot vessel's True course and distance run for time interval from assumed position (water track).

**Step 4:** Apply tidal vector from end of water track (same duration).

**Step 5:** Take second bearing of same object, convert to True, plot.

**Step 6:** Transfer first bearing line (parallel) to end of tidal vector without moving its orientation.

**Step 7:** Intersection of transferred line and second bearing = FIX

**Key Principle:** Initial position guess doesn't matter - transferred line will always create correct fix regardless of starting point.

## Common Errors
- Not transferring first bearing parallel to original
- Forgetting to apply tidal vector before transferring
- Changing course between bearings (invalidates fix)
- Measuring from wrong point on bearing line

## Assessment
- Plot running fix with ±0.3 NM accuracy
- Demonstrate fix works from two different assumed positions
- Calculate fix for 1-hour run with tidal set
- Explain mathematical principle of transferred lines