# Plugin 01: Chart Basics

**RYA/ASA YachtMaster – Chart Fundamentals, Datums, Symbols & Compass**

## What This Plugin Teaches
- Geodetic datums (GPS ↔ Chart compatibility checks)
- Vertical datums (HAT, MHWS, CD, LAT, MSL)
- Chart symbols and abbreviations (INT 1 / 5011)
- Mercator projection basics
- Compass errors (variation & deviation)
- Chart corrections and currency (Notices to Mariners, updating charts)

## Skills Included (18 total)

**Chart Fundamentals & Datums (4)**
1. **datum-guardian** - GPS/chart datum compatibility and shift calculations
2. **charted-height-interpreter** - Vertical datum reference guide
3. **chartwork-mercator-projection** - Explains Mercator projection principles
4. **longitude-latitude** - How to read and use lat/long scales correctly

**Chart Symbols & Quizzes (3)**
5. **symbol-spotter** - Interactive chart symbol quiz with 100+ symbols
6. **chart-symbol-spotter** - Identify chart symbols by name or photo
7. **symbol-quiz-flashcards** - Rapid-fire flashcard quiz on chart symbols

**Chart Corrections & Currency (5)**
8. **chart-correction-decoder** - Read and explain chart correction panels
9. **chart-update-checker** - Verify chart currency and identify required corrections
10. **chart-update-checklist** - Shopping list and steps for hand-correcting charts
11. **chart-safe-go-nogo** - Quick safety call on chart currency
12. **corrections-mini-quiz** - Interactive quiz on reading correction panels
13. **photo-correction-reader** - OCR and decode correction photos

**Compass Errors & Corrections (5)** ✨ NEW
14. **magnetic-variation-calculator** - Calculate current variation from compass rose with annual change
15. **compass-error-correction** - True ↔ Magnetic ↔ Compass conversion using CADET
16. **compass-deviation-table** - Use ship's deviation table with interpolation
17. **hand-bearing-compass** - Position fixing and collision avoidance techniques
18. **compass-dip-heeling** - Magnetic dip, hemisphere balancing, heeling error awareness

## Agent
**Chart Basics Tutor** - Patient instructor focusing on precision and safety

## How to Use
Activate by asking chart-related questions:
- "Can I plot WGS-84 onto BA 2454?"
- "Is that lighthouse height above HAT or MHWS?"
- "Test me on chart symbols"
- "Convert 085°T to compass, variation 5°W, deviation +2°E"
- "Read this chart correction: 2007-547 2008-1120 2009-1716"
- "Is this chart safe to use?"
- "How do I update my chart?"

## Status
✅ **Ready for Testing** - 18 skills fully implemented (13 original + 5 compass skills added)

## Example Session
```
User: "Can I plot WGS-84 straight onto BA 2454?"

Agent: Let me check the geodetic datum compatibility for you.

✅ SAFE TO PLOT

BA 2454 (Approaches to Portsmouth) uses WGS-84 geodetic datum.
Your GPS is also WGS-84.

→ No shift required - plot position directly as read from GPS.

Always check chart title block for datum before plotting.
```

## Version
v0.2.0 (2025-11-10) - Added 5 compass skills: magnetic-variation-calculator, compass-error-correction, compass-deviation-table, hand-bearing-compass, compass-dip-heeling
v0.1.2 (2025-11-02) - Added 5 chart skills: chart-symbol-spotter, chart-update-checker, chartwork-mercator-projection, longitude-latitude, symbol-quiz-flashcards
