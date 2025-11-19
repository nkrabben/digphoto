---
title: "GoPro Action Camera File Naming Conventions"
manufacturer: GoPro
device_type: Camera, 360
topic: file-naming
last_verified: 2024-11-19
confidence: high

patterns:
  - pattern: "GOPR####.jpg"
    description: "Single photo"
    models: "Hero 1-5"

  - pattern: "G*_####.ext"
    description: "Single photo"
    models: "Hero 6+"

  - pattern: "G*######.jpg"
    description: "Time-lapse or burst photos"
    models: "All GoPro cameras"

  - pattern: "G*XX####.mp4"
    description: "Video file"
    models: "All Hero cameras"

tags:
  - naming
  - action-camera
  - gopro
---

GoPro has used a few file-name schemas to indicate the type of image or video within the file. Generally, filenames begin with `G` and ends with a 4-digit counter and lower-case extension. These file names are inspired by DCF, but can have variable information after the `G`.

## Standard Pattern: G*XX####.ext

- Format: `G*XX####.ext`
- Second character: may indicate codec
- First counter: Used for chaptering video files or counting burst photos
- Second counter: Increments across all file types
- Extension: varies on content type

### Images

#### Single Photo

- Pattern: `G*_####.jpg`
- Example: `GS_1234.jpg`
- Notes:
  - `S` for images, `P` for panoramas
  - Can be used for 360 photos as well

#### Burst Photo

- Pattern: `GXXX####.ext`
- Example: `G0011235000.jpg` to `G0011287.jpg`

### Videos

For many reasons, GoPros limit file-sizes to 4 GB. After that a new file is created with a chapter number in the third and fourth characters.

#### Standard Video

- Pattern: `G*XX####.mp4`
- Example: `GX011000.mp4`
- Notes:
  - `X` for HEVC, `H` for H264, `P` for older videos
  - `XX` is numbering for chapters or loops

#### 360 Video

- Pattern: `GSXX####.360`
- Example: `GS011001.360`
- Notes:
  - `XX` is numbering for chapters or loops

## Sources

[GoPro Community Guide on File Names](https://community.gopro.com/s/article/GoPro-Camera-File-Naming-Convention?language=en_US)
