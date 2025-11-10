# SKILL: Light Ranges and Radar Beacons (SKILL_74)

## Description
Calculate and apply light visibility ranges including geographical, luminous, and nominal ranges, and identify radar beacons (RACON) for electronic navigation assistance.

## Prerequisites
- Navigation Light Characteristics (SKILL_73)

## Learning Objectives
- Distinguish between three types of light range
- Calculate dipping distance mathematically
- Use dipping tables for position fixing
- Identify and interpret RACON signals
- Apply range information for navigation planning

**Types of Light Range:**

**Geographical Range:**
- **Definition:** Extreme distance based on line of sight (Earth's curvature)
- **Factors:** Height of eye, height of light, weather
- **Formula:** 2.08 × √height of eye + 2.08 × √height of light (in nautical miles)
- **Use:** Calculate when light should become visible when approaching

**Luminous Range:**
- **Definition:** Greatest distance visible based on light intensity and visibility
- **Factors:** Luminous intensity, atmospheric clarity
- **Variable:** Changes with weather conditions

**Nominal Range:**
- **Definition:** Luminous range for visibility of 10 nautical miles (standard reference)
- **Chart Information:** Usually listed as "Visible up to X miles"
- **Reduction:** Decreases as visibility reduces below 10 miles
- **Example:** "10M" means 10 mile nominal range

**Practical Range Example:**
- **Large vessel** (10m height of eye) sees 24M light sooner than **small vessel** (2m height of eye)
- **Dipping distance:** When light first appears/disappears on horizon with vessel motion

**Dipping Light Formula:**

Distance (nm) = 2.08 × √(Height of Eye in meters) + 2.08 × √(Height of Light in meters)
Copy

**Dipping Table Use:**
1. Obtain light height from chart/almanac
2. Estimate height of eye on your vessel
3. Apply formula or use pre-calculated tables
4. Take bearing when light first appears for position fix

**RACON (Radar Beacon):**
- **Definition:** Transponder beacon transmitting coded signal on radar frequency
- **Function:** Permits interrogating craft to determine bearing and range
- **Frequencies:**
  - 3cm (X-band): 9300-9500 MHz
  - 10cm (S-band): 2900-3100 MHz
- **Radar Display:** Appears as Morse code pattern on radar screen
- **Identification:** Morse character appears at same range as RACON

**Practical Application:**
Use dipping distance calculation for offshore position fixing when GPS unreliable or to verify position.

## Common Errors
- Confusing geographical vs luminous vs nominal range
- Using nominal range as guaranteed visibility distance
- Forgetting to add height of tide for light height calculations
- Misidentifying RACON Morse code on radar
- Not accounting for reduced visibility in fog/haze

## Assessment
- Calculate dipping distance for given heights
- Explain difference between range types
- Determine when specific light should become visible
- Identify RACON on radar display
- Apply range knowledge for passage planning

***