---
title: "Canon File Naming Conventions"
manufacturer: Canon
device_type: Camera
topic: file-naming
last_verified: 2024-11-18
confidence: high

patterns:
  - pattern: "IMG_####.JPG"
    description: "Standard JPEG naming"
    counter_range: "0001-9999"
    resets_on: ["memory card format", "camera factory reset"]
    models: "Most EOS models"

  - pattern: "IMG_####.CR2"
    description: "RAW files (2004-2018)"
    years: "2004-2018"
    models: ["5D Mark II", "7D", "5D Mark III", "5D Mark IV"]

  - pattern: "IMG_####.CR3"
    description: "RAW files (2018+)"
    years: "2018-present"
    models: ["R5", "R6", "R7", "R10"]

  - pattern: "IMG_E####.JPG"
    description: "In-camera edited JPEG"
    notes: "E prefix indicates edit applied"

  - pattern: "_MG_####.CR2"
    description: "Alternative RAW naming (some older models)"
    models: ["5D Mark II (early firmware)"]

forensic_indicators:
  - indicator: "Counter reset to 0001"
    meaning: "Memory card formatted or camera factory reset"
  - indicator: "IMG_E prefix"
    meaning: "Image edited in-camera (crop, resize, filter)"
  - indicator: "Gaps in sequence"
    meaning: "Deleted files or selective transfer"

tags:
  - naming
  - forensics
---

# Canon File Naming Conventions

Canon uses a consistent naming pattern across most of their cameras, with some variations for professional video equipment.

## Standard Pattern: IMG_####

The most common pattern across Canon EOS cameras is:
- Format: `IMG_####.EXT`
- Counter: 0001-9999
- Resets: When memory card is formatted or counter reaches 9999

### JPEG Files
Standard JPEG files use `IMG_####.JPG` with sequential numbering.

### RAW Files

Canon has used two RAW formats:

CR2 (2004-2018):
- Used in most EOS DSLRs
- Pattern: `IMG_####.CR2`
- Some early models used `_MG_####.CR2`

CR3 (2018-present):
- Introduced with EOS R system
- Pattern: `IMG_####.CR3`
- More efficient compression
- Better metadata support

## In-Camera Edits

Files with `IMG_E####.JPG` pattern indicate in-camera editing:
- Resize
- Crop
- Creative filters applied
- Forensic note: Original file may still exist with base number

## Professional Video (Cinema EOS)

Cinema cameras use different naming:
- Pattern: `C####.MXF`
- Folder: `CONTENTS/CLIPS###/`
- See [Canon Video Formats](../video-codecs/) for details
