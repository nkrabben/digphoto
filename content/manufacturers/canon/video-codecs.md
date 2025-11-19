---
title: "Canon Video Codecs"
manufacturer: Canon
device_type: Camera
topic: video-codecs
last_verified: 2024-11-18

codecs:
  - name: "Motion JPEG"
    introduced: 2008
    first_models: ["5D Mark II"]
    container: "MOV"
    notes: "First DSLR video, low compression"

  - name: "H.264"
    introduced: 2009
    first_models: ["7D", "5D Mark III"]
    container: "MOV"
    bitrate: "Up to 90 Mbps (All-I)"

  - name: "H.265 (HEVC)"
    introduced: 2020
    first_models: ["R5", "R6"]
    container: "MP4"
    bitrate: "Up to 470 Mbps (8K)"
    notes: "4K/8K capability"

tags:
  - video
  - codecs
---

# Canon Video Codecs

Canon's video codec journey from Motion JPEG to modern HEVC.

## Timeline

### 2008: Motion JPEG (5D Mark II)
Revolutionary but inefficient...

### 2009-2019: H.264 Era
Standard codec across EOS line...

### 2020+: H.265/HEVC
Introduced with mirrorless systems...

## Forensic Dating
A file claiming to be from 2015 with H.265 codec is either:
- Misdated (camera clock wrong)
- Transcoded after capture
- Falsified metadata