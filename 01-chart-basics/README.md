# Plugin 01: Chart Basics

**RYA/ASA YachtMaster – Chart Fundamentals, Datums, Symbols & Compass**

## What This Plugin Teaches
- Geodetic datums (GPS ↔ Chart compatibility checks)
- Vertical datums (HAT, MHWS, CD, LAT, MSL)
- Chart symbols and abbreviations (INT 1 / 5011)
- Mercator projection basics
- Compass errors (variation & deviation)
- Chart corrections and currency (Notices to Mariners, updating charts)

## Skills Included
1. **chart-correction-decoder** - Read and explain chart correction panels
2. **charted-height-interpreter** - Vertical datum reference guide
3. **chart-safe-go-nogo** - Quick safety call on chart currency
4. **chart-symbol-spotter** - Identify chart symbols by name or photo
5. **chart-update-checker** - Verify chart currency and identify required corrections
6. **chart-update-checklist** - Shopping list and steps for hand-correcting charts
7. **chartwork-mercator-projection** - Explains Mercator projection principles
8. **corrections-mini-quiz** - Interactive quiz on reading correction panels
9. **datum-guardian** - GPS/chart datum compatibility and shift calculations
10. **longitude-latitude** - How to read and use lat/long scales correctly
11. **photo-correction-reader** - OCR and decode correction photos
12. **symbol-quiz-flashcards** - Rapid-fire flashcard quiz on chart symbols
13. **symbol-spotter** - Interactive chart symbol quiz with 100+ symbols

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
✅ **Ready for Testing** - 13 skills fully implemented

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
v0.1.2 (2025-11-02) - Added 5 new skills: chart-symbol-spotter, chart-update-checker, chartwork-mercator-projection, longitude-latitude, symbol-quiz-flashcards
