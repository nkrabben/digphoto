---
title: "GoPro Proxies"
manufacturer: GoPro
device_type: Camera, 360
topic: proxies
last_verified: 2024-11-20
confidence: low

tags:
  - proxies
  - gopro
---

GoPro Cameras create low-resolution proxy files, primarily for on-device previews. They are stored in the same folder as the original file.

## Images and Video

## THM (Thumbnail)

- File Name Pattern: `XX######.THM`
- Purpose: On-device preview
- Container: EXIF
- Codec: JPEG
- Resolution: 160x120
- Correspondence: Same name as original except extension.
  - Example: `GH010078.MP4` has `GH010078.THM`

## Video

### LRV (Low-Resolution Video)

- File Name Pattern: Same as original `GL######.LRV`
- Purpose: On-device preview, proxy editing
- Container: MP4
- Codec: H264 or HEVC
- Resolution: 240p, 480p
- Correspondece: Same counter as original
  - Example: `GH010078.MP4` has `GL010078.LRV`
