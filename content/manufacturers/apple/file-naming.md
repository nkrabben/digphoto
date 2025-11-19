---
title: "Apple iPhone File Naming Conventions"
manufacturer: Apple
device_type: Phone, Tablet
topic: file-naming
last_verified: 2024-11-18
confidence: medium

patterns:
  - pattern: "IMG_####.EXT"
    description: "All media uses the same counter"
    counter_range: "0001-9999"
    models: "All iPhones and iPads"

tags:
  - naming
  - mobile
  - apple
---

Apple maintains consistent file naming across iPhone and iPad generations that applies to all content types.

## Standard Pattern: IMG_####

- Format: `IMG_####.EXT`
- Counter: 0001-9999
- Extension: varies on content type

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

