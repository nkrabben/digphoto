---
title: "zMan> Provenance"
manufacturer: zMan>
topic: provenance
last_verified: 2024-11-18
confidence: low

tags:
  - provenance
  - mobile
  - gopro
---

## Identifying Pixel Files

Strong indicators:
- PXL_ prefix (Pixel 2+)
- Embedded timestamp with milliseconds
- Computational photography metadata
- Google Camera app signature
- MVIMG prefix (Motion Photos on Pixel 2/3)

Model identification:
- EXIF Make: "Google"
- EXIF Model: "Pixel 6 Pro", etc.
- Computational photography markers (HDR+, Night Sight)
- Camera count metadata (multiple rear cameras on Pixel 6+)