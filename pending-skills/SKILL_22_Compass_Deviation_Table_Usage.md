# SKILL: Compass Deviation Table Application

## Description
Use ship's compass deviation table to correct for magnetic interference from vessel's equipment and structure.

## Prerequisites
- Understanding of compass errors
- Access to vessel's deviation table

## Learning Objectives
- Locate deviation for given compass heading
- Interpolate deviation between table values
- Apply deviation corrections correctly
- Understand deviation table limitations

## Deviation Table Interpretation
**Structure:**
- Left column: Compass heading (usually 15° increments)
- Right column: Deviation (E or W)

**Usage Rules:**
- Compass to Magnetic: Add East, Subtract West
- Magnetic to Compass: Subtract East, Add West

**Interpolation:**
- For headings between table values (&gt;1° difference)
- Example: 81° (between 67.5° and 90°)
- 67.5° = 2°E, 90° = 4°E
- 81° is 60% between them: ~3°E

## Common Errors
- Using table backwards (M→C vs C→M)
- Not interpolating when needed (off by 1-2°)
- Forgetting deviation changes with heading
- Applying same deviation to hand bearing compass

## Assessment
- Find deviation for 8 random compass headings
- Interpolate 3 values between table entries
- Explain why deviation is specific to fixed compass location