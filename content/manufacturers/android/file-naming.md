---
title: "Android File Naming Conventions"
manufacturer: Android
topic: file-naming
last_verified: 2024-11-18
confidence: medium

patterns:
  - pattern: "IMG_YYYYMMDD_HHMMSS.jpg"
    description: "AOSP default JPEG pattern"
    models: "Stock Android devices"

  - pattern: "YYYYMMDD_HHMMSS.jpg"
    description: "Alternative timestamp pattern"
    models: "Various Android devices"

  - pattern: "VID_YYYYMMDD_HHMMSS.mp4"
    description: "AOSP default video pattern"
    models: "Stock Android devices"

  - pattern: "IMG_####.jpg"
    description: "Simple counter pattern (older devices)"
    counter_range: "0001-9999"
    models: "Older stock Android devices"

  - pattern: "DSC####.jpg"
    description: "Digital camera style (some manufacturers)"
    counter_range: "0001-9999"
    models: "Various Android devices"

tags:
  - naming
  - mobile
  - android
---

Android's open ecosystem means file naming vary across manufacturers and models.

Android photos tend to use lower-case `.jpg`.

## Standard Patterns: TYPE_yyyyMMdd_HHmmss.EXT

Stock AOSP (Android Open Source Project) devices use timestamp-based naming:

### Photos

- Pattern: `IMG_YYYYMMDD_HHMMSS.jpg`
- Example: `IMG_20241118_143022.jpg`

### Videos

- Pattern: `VID_YYYYMMDD_HHMMSS.mp4`
- Example: `VID_20241118_143022.mp4`

## Common Alternative Patterns

### Date-Only Format

- Pattern: `YYYYMMDD_HHMMSS.jpg`
- Example: `20241118_143022.jpg`
- Used by: Samsung, some Chinese manufacturers

### Simple Counter

- Pattern: `prefix####.jpg`
- Examples: `IMG_9852.jpg`, `DSC0001.jpg`
- Used by: budget phones

## Screenshots

Screenshot file names look very similar to camera file names except, they use `Screenshot` as a prefix, separate data and time with a `-`, and use `.png` since they are PNG files

- Pattern: `Screenshot_yyyyMMdd_HHmmss.png`
- Example: `Screenshot_20220902-154332.jpg`

## Third-Party Camera Apps

Third-party camera apps may follow their own file-naming schema although they generally use either DCF- or Android timestamp-style file names.

## Sources

[Android Developer Docs](https://developer.android.com/media/camera/camerax/video-capture#configure-and-create-recording) - Example showing how to name a file with a timestamp