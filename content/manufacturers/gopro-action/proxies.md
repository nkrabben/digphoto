---
title: "GoPro Proxies"
manufacturer: GoPro
device_type: Action
topic: proxies
last_verified: 2024-11-18
confidence: low

tags:
  - proxies
  - mobile
  - gopro
---

## Proxy and Metadata Files

### LRV (Low-Resolution Video)
- Pattern: `GL######.LRV`
- GL: GoPro Low-res
- Purpose: Quick preview, proxy editing
- Resolution: Typically 240p or 480p
- Codec: Usually H.264 at low bitrate
- Matches: Same number as main MP4
- Example: `GH010078.MP4` has `GL010078.LRV`

### THM (Thumbnail)
- Pattern: `GH######.THM` or `GP######.THM`
- Purpose: Video thumbnail for camera playback
- Format: JPEG (usually 160x120 or similar)
- Matches: Corresponding video file
- Example: `GH010078.MP4` has `GH010078.THM`