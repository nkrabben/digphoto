---
title: "GoPro Action Camera File Naming Conventions"
manufacturer: GoPro
device_type: Action
topic: file-naming
last_verified: 2024-11-18
confidence: high

patterns:
  - pattern: "GOPR####.JPG"
    description: "Single photo"
    models: "All GoPro cameras"

  - pattern: "GP######.JPG"
    description: "Time-lapse or burst photos"
    models: "All GoPro cameras"

  - pattern: "GH######.MP4"
    description: "Video file (first in series)"
    models: "Hero4 and later"

  - pattern: "GP######.MP4"
    description: "Video continuation (chapter file)"
    models: "Hero4 and later"

  - pattern: "GL######.LRV"
    description: "Low-resolution video proxy"
    models: "Hero4 and later"

  - pattern: "GH######.THM"
    description: "Video thumbnail image"
    models: "All GoPro cameras"

forensic_indicators:
  - indicator: "GOPR prefix"
    meaning: "GoPro single photo"
  - indicator: "GH/GP chapter sequence"
    meaning: "Multi-part GoPro video"
  - indicator: "LRV files present"
    meaning: "GoPro video with proxy files"
  - indicator: "THM thumbnail files"
    meaning: "GoPro video metadata"

tags:
  - naming
  - forensics
  - action-camera
  - video
---

# GoPro Action Camera File Naming Conventions

GoPro uses a distinctive naming system designed for high-volume capture with chaptered video files and low-resolution proxies.

## Photo Naming

### Single Photos
- Pattern: `GOPR####.JPG`
- GOPR: GoPro Photo
- Counter: 4-digit (0001-9999)
- Usage: Single shots, not burst/time-lapse

### Burst and Time-Lapse Photos
- Pattern: `GP######.JPG`
- 6-digit counter: Accommodates high frame counts
- Sequential: Increments for each frame
- Example: `GP010001.JPG`, `GP010002.JPG`...

### RAW Photos
- Pattern: `GOPR####.GPR` (Hero5 Black and later)
- GPR: GoPro RAW format (DNG-based)
- Availability: SuperPhoto mode or Pro RAW
- Models: Hero5 Black, Hero6, Hero7, Hero8+

## Video Naming System

GoPro's video naming is complex due to file chaptering:

### First Video File (Chapter 1)
- Pattern: `GH######.MP4`
- GH: GoPro High quality
- 6 digits: Session and file number
- Example: `GH010078.MP4` (first chapter of video 78)

### Continuation Files (Chapters 2+)
- Pattern: `GP######.MP4`
- GP: GoPro (continuation)
- Same number: Matches first chapter
- Example:
  - `GH010078.MP4` (chapter 1, 4GB)
  - `GP020078.MP4` (chapter 2, 4GB)
  - `GP030078.MP4` (chapter 3, remaining)

### Why Chaptering?

Video files split due to:
- FAT32 limit: 4GB file size maximum
- Codec limits: Some codecs have duration limits
- Processing: Easier to handle smaller files
- Compatibility: Older systems handle better

### Chapter Numbering
- 01, 02, 03: Chapter number in first two digits
- Same base: Last 4 digits match across chapters
- Sequential playback: Must concatenate for full video



## Time Code and Telemetry

Modern GoPros embed metadata:
- GPS data: Latitude, longitude, altitude
- Accelerometer: Motion data
- Gyroscope: Rotation data
- Telemetry: Speed, G-force
- No separate file: Embedded in MP4

### GPMF (GoPro Metadata Format)
- Embedded track: In MP4 file
- Extraction: Requires special tools
- Data types: GPS, IMU, audio levels, exposure
- Analysis: Can visualize path, speed, etc.


