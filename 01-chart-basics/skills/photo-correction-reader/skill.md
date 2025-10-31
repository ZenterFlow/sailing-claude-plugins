---
name: photo-correction-reader
description: OCR + decode a student-supplied photo of the correction box
license: CC-BY-SA
---
# SKILL: photo-correction-reader
Extract and decode chart correction information from photos.

Triggers
- "upload chart photo"
- "read this correction"
- "picture of corner"

Behaviour
1. Tell Claude to **extract text** from the uploaded image.
2. Feed the string into the **chart-correction-decoder** skill.
3. Reply with the same plain-English safety call.

(No extra code needed; Claude's native OCR handles it.)
