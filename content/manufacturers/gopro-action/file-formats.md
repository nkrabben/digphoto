---
title: "GoPro File Formats"
manufacturer: GoPro
device_type: Camera, 360
topic: file-formats
last_verified: 2024-11-20
confidence: high

tags:
  - formats
  - gopro
---

GoPro cameras write additional metadata to record the state of the camera, particularly to their video files.

## Images

### JPEG

- Container: EXIF
- Codec: JPEG

## Video

### GoPro MP4

- Container: MPEG-4
- Codec: H264 or HEVC
- Tracks:
  - GoPro MET - for GPS, accelerometer, and other sensor data
  - GoPro TC - for timecode
  - 1 video track
  - 1 audio track
  - GoPro SOS - for file recovery

### 360 files

- Container: MPEG-4
- Codec: H264 or HEVC
- Tracks:
  - GoPro MET - for GPS, accelerometer, and other sensor data
  - GoPro TCD - for timecode
  - 2 video tracks
  - 2 audio tracks
  - GoPro SOS - for file recovery

### General Purpose Metadata Format (GPMF)

The GoPro metadata track is a MP4 atom used to store a variety of metadata including:

- camera setting: ISO, shutter, white balance, etc
- telemetry: GPS, UTC, etc
- face tracking
- microphone condition

GoPro changes the specific fields with nearly every generation since the GoPro 4.

## Sources

[GPFM-Parser](https://github.com/gopro/gpmf-parser?tab=readme-ov-file#gopros-mp4-structure)
