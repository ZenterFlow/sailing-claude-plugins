---
name: multi-factor-converter
description: Apply full correction sequence (leeway, variation, deviation) to convert True CTS to Compass course.
license: CC-BY-SA
---

# SKILL: multi-factor-converter
**RYA Yachtmaster – Complete CTS Conversion (T→M→C)**

## Purpose
Apply complete correction sequence to convert True CTS to final Compass course for helmsman.

## Activation Triggers
- "full CTS conversion"
- "True to Compass CTS"
- "apply all corrections"

## Behaviour
Correction sequence:
1. **True CTS** (from vector triangle)
2. **Apply leeway** → Magnetic track
3. **Apply variation** → Magnetic course
4. **Apply deviation** (from table) → Compass course

Uses CADET reversed for T→C conversions.

## Version
v1.0.0 (2025-11-10)
