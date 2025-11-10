# Plugin 01: Chart Basics

**RYA/ASA YachtMaster – Chart Fundamentals, Datums, Symbols & Compass**

## What This Plugin Teaches
- Geodetic datums (GPS ↔ Chart compatibility checks)
- Vertical datums (HAT, MHWS, CD, LAT, MSL)
- Chart symbols and abbreviations (INT 1 / 5011)
- Mercator projection basics
- Compass errors (variation & deviation)
- Chart corrections and currency (Notices to Mariners, updating charts)

## Skills Included (17 total)

### Chart Datum & Positioning (4 skills)
1. **datum-guardian** - GPS/chart datum compatibility and shift calculations
2. **charted-height-interpreter** - Vertical datum reference guide (HAT, MHWS, CD, LAT)
3. **longitude-latitude** - How to read and use lat/long scales correctly
4. **chartwork-mercator-projection** - Explains Mercator projection principles

### Chart Symbols & Identification (3 skills)
5. **symbol-spotter** - Interactive chart symbol quiz with 100+ symbols
6. **symbol-quiz-flashcards** - Rapid-fire flashcard quiz on chart symbols
7. **chart-symbol-spotter** - Identify chart symbols by name or photo

### Chart Corrections & Currency (6 skills)
8. **chart-correction-decoder** - Read and explain chart correction panels
9. **corrections-mini-quiz** - Interactive quiz on reading correction panels
10. **chart-update-checklist** - Shopping list and steps for hand-correcting charts
11. **chart-update-checker** - Verify chart currency and identify required corrections
12. **chart-safe-go-nogo** - Quick safety call on chart currency
13. **photo-correction-reader** - OCR and decode correction photos

### Compass Errors & Corrections (4 skills - NEW in v0.3.0)
14. **magnetic-variation-calculator** - Calculate current variation from compass rose with annual change
15. **compass-error-corrector** - Convert True ↔ Magnetic ↔ Compass using CADET mnemonic
16. **deviation-table-reader** - Read and interpolate ship's deviation table for any heading
17. **hand-bearing-compass-guide** - Hand bearing compass technique, position fixing, collision avoidance

## Agent
**Chart Basics Tutor** - Patient instructor focusing on precision and safety

## How to Use
Activate by asking chart-related questions:

### Datum & Position
- "Can I plot WGS-84 onto BA 2454?"
- "Is that lighthouse height above HAT or MHWS?"
- "How do I measure latitude from the chart?"

### Symbols
- "Test me on chart symbols"
- "What does this symbol mean?" (with photo)

### Compass
- "Calculate variation for 2025 from this compass rose"
- "Convert 085°T to compass, variation 5°W, deviation +2°E"
- "Find deviation for heading 081°M"
- "How do I take a hand bearing compass fix?"

### Corrections
- "Read this chart correction: 2007-547 2008-1120 2009-1716"
- "Is this chart safe to use?"
- "How do I update my chart?"

## Status
✅ **Complete** - 17 skills fully implemented (100% coverage of RYA/ASA chart basics syllabus)

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

## Version History

**v0.3.0** (2025-11-10)
- Added 4 compass error skills for complete compass workflow
- magnetic-variation-calculator: Calculate variation from compass rose with annual change
- compass-error-corrector: Full T ↔ M ↔ C conversions with CADET mnemonic
- deviation-table-reader: Read and interpolate deviation tables
- hand-bearing-compass-guide: Position fixing and collision avoidance techniques
- Plugin now complete with 17 skills (100% RYA/ASA chart basics syllabus)

**v0.1.2** (2025-11-02)
- Added 5 skills: chart-symbol-spotter, chart-update-checker, chartwork-mercator-projection, longitude-latitude, symbol-quiz-flashcards

**v0.1.0** (2025-10-31)
- Initial release with 8 skills
