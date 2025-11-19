---
title: "Apple iPhone File Naming Conventions"
manufacturer: Apple
device_type: iPhone, iPad
topic: file-naming
last_verified: 2024-11-18
confidence: medium

patterns:
  - pattern: "IMG_####.HEIC"
    description: "Standard HEIC photo (iOS 11+)"
    counter_range: "0001-9999"
    models: "iPhone 7 and later (iOS 11+)"

  - pattern: "IMG_####.JPG"
    description: "JPEG photo (older iOS or compatibility mode)"
    counter_range: "0001-9999"
    models: "All iPhones"

  - pattern: "IMG_####.MOV"
    description: "Video file or Live Photo video component"
    models: "All iPhones"

  - pattern: "IMG_E####.HEIC"
    description: "Edited photo"
    models: "iOS 11+"

  - pattern: "IMG_####.PNG"
    description: "Screenshot"
    models: "All iPhones"

forensic_indicators:
  - indicator: "HEIC extension"
    meaning: "iPhone 7+ with iOS 11+, or newer iPhone"
  - indicator: "IMG_E prefix"
    meaning: "Photo edited in Photos app"
  - indicator: "Paired HEIC and MOV"
    meaning: "Live Photo (3-second video + photo)"
  - indicator: "PNG with specific dimensions"
    meaning: "Screenshot (varies by iPhone model)"

tags:
  - naming
  - forensics
  - mobile
---

Apple maintains consistent file naming across iPhone and iPad generations that applies to all content types.

## Standard Pattern: IMG_####

Apple's simple, consistent pattern:
- Format: `IMG_####.EXT`
- Counter: 0001-9999
- Extension: varies on content type
-
### Images

- Pattern: `IMG_####.HEIC`
- Example: `IMG_6879.HEIC`
- Usage:
  - iPhones after iOS 10

- Pattern: `IMG_####.JPG`
- Example: `IMG_6880.JPG`
- Usage:
  - iPhones before iOS 11
  - Compatibility mode ("Most Compatible" setting)

- Pattern: `IMG_####.DNG`
- Example: `IMG_6881.DNG`
- Usage:
  - iPhones after iOS 12
  - Must be enabled

- Pattern: `IMG_####.PNG`
- Example: `IMG_6882.PNG`
- Usage:
  - Screenshots

## Video Files

- Pattern: `IMG_####.MOV`
- Example: `IMG_6883.MOV`

## Live Photos

Viewable as one asset within the Photos app, but actually two distinct files.

Components:

- Pattern: `IMG_####.MOV` + `IMG_####.HEIC` or `IMG_####.JPG`
- Example: `IMG_6884.MOV` + `IMG_6884.HEIC`

## Edited

When edited in Photos app:

- Pattern: `IMG_E####.EXT`
- Example: `IMG_E6879.HEIC`

## Sources

