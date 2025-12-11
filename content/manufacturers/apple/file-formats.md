---
title: "Apple File Formats"
manufacturer: Apple
device_type: Phone, Tablet
topic: file-formats
last_verified: 2024-11-18
confidence: medium

patterns:
  - pattern: "HEIF, MOV, JPEG, DNG"

tags:
  - formats
  - mobile
  - apple
---

## Images

### High Efficiency Image Format (HEIC)

- Introduced: iOS 11 (2017)
- Container: HEIF
- Codec: HEVC
- Notes:
  - Greater compression efficiency for a given quality
  - Apps may convert to JPEG for compatibility purposes
  - Used for Spatial Images. Each image is stored as a separate track with metadata identifying the lens

### JPEG

- Container: JFIF
- Codec: JPEG DCT
- Notes:
  - Must be actively chosen by users on modern iPhones

### ProRAW (DNG)

- Introduced: iOS 11 (2017)
- Container: TIFF (Adobe DNG)
- Codec: ProRAW
- Notes:
  - Must be actively chosen by users
  - Can be generated simultaneously with HEIF or JPEG

## Video

### Quicktime File (MOV)

- Container: MPEG-4
- Codec: HEVC
- Notes:
  - Used H264 until
  - May be identified as an MP4 with a Quicktime Profile
  - Used for Spatial Video. Each image is stored as a separate track with metadata identifying the lens
