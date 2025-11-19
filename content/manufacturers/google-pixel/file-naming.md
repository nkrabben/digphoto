---
title: "Google Pixel File Naming Conventions"
manufacturer: Google
device_type: Phone
topic: file-naming
last_verified: 2024-11-18
confidence:

patterns:
  - pattern: "PXL_yyyyMMdd_HHmmssSSS.TYPE.ext"
    description: "All media types"
    models: "Pixel 5 and later"

  - pattern: "IMG_YYYYMMDD_HHMMSS.jpg"
    description: "Image"
    models: "Pixel 1-4"

  - pattern: "MVIMG_YYYYMMDD_HHMMSS.jpg"
    description: "Motion Photo"
    models: "Pixel 1-4"

tags:
  - naming
  - mobile
  - android
---

Beginning with the Camera v7.5 in 2020, Google created a more distinctive file naming schema based on the Android timestamp filename. This roughly aligns with the release of the Pixel 5. Earlier Pixels could update to that software.

## Standard Pattern: PXL_yyyyMMdd-HHmmssSSS.TYPE.ext

- Format: `PXL_yyyyMMdd_HHmmssSSS.TYPE.ext`
- Timestamp: UTC, may include milliseconds, depending on content
- Variants: Shortcodes for non-standard images
- Extension: varies on content type

### Images

#### Standard Photo

- Pattern: `PXL_yyyyMMdd_HHmmss.TYPE.jpg`
- Example: `PXL_20231223_180634.jpg`
- Usage:
  - Pixel 5 and later

Types include HDR, PORTRAIT, COVER, NIGHT

#### Burst Photo

- Pattern: `PXL_yyyyMMdd_HHmmssSSS.jpg`
- Example: `PXL_20231223_180635782.jpg`

#### RAW Photo

- Pattern: `PXL_yyyyMMdd_HHmmss.dng`
- Example: `PXL_20231223_180636.dng`
- Notes:
  - Pixel 5 and later
  - Timestamp matches jpg if shot together
  - Must be enabled

#### Screenshots

- Pattern: `Screenshot_yyyyMMdd-HHmmss.png`
- Example: `Screenshot_20231223-180637.png`
- Notes:
  - Timestamp may be in local timezone, not UTC

### Videos

- Pattern: `PXL_yyyyMMdd_HHmmss.mp4`
- Example: `PXL_20231223_180638.mp4`

### Live Photos

#### Single File

- Pattern: `PXL_YYYYMMDD_HHMMSS.MP.jpg`
- Example: `PXL_20231223_180639.MP.jpg`
- Notes:
  - Pixel 5 and later
  - File is actually two files concatenated

#### Paired Files

Viewable as one asset within the Photos app, but actually two distinct files.

Components:

- Pattern: `MVIMG_YYYYMMDD_HHMMSS.mp4` + `MVIMG_YYYYMMDD_HHMMSS.jpg`
- Example: `MVIMG_20191223_180640.mp4` + `MVIMG_20191223_180640.jpg`
- Notes:
  - Pixel 1-4

## Sources

[Soon, everyone you share photos and videos with will know you've got a Pixel](https://www.androidpolice.com/2020/08/20/soon-everyone-you-share-photos-and-videos-with-will-know-youve-got-a-pixel/), Android Police



