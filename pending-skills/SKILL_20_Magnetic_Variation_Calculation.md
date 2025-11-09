# SKILL: Magnetic Variation Calculation

## Description
Calculate current magnetic variation using chart compass rose data and annual change rates.

## Prerequisites
- Chart reading fundamentals
- Basic arithmetic with degrees/minutes

## Learning Objectives
- Read variation data from compass rose
- Apply annual change rate for specific year
- Calculate variation to nearest degree
- Account for east/west movement correctly

## Calculation Method
**Formula:**
Variation_Target_Year = Variation_Base_Year ± (Rate × Years)

**Rules:**
- West variation with East movement: SUBTRACT movement
- West variation with West movement: ADD movement
- East variation with West movement: SUBTRACT movement
- East variation with East movement: ADD movement

**Example (from compass rose):**
- 2005 variation: 7° 25' W
- Annual change: 8' E (moving east)
- Target year: 2007 (2 years later)
- Calculation: 7° 25' W - (8' × 2) = 7° 09' W

## Common Errors
- Adding when should subtract (and vice versa)
- Forgetting variation moves opposite direction for east/west
- Not rounding to nearest degree for practical use
- Using wrong base year from rose

## Assessment
- Calculate variation for 5 positions/years with 100% accuracy
- Complete within 3 minutes per calculation
- Explain directional logic without reference