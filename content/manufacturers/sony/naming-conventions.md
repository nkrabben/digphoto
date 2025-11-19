---
title: "Sony File Naming Conventions"
manufacturer: Sony
device_type: Camera
topic: file-naming
last_verified: 2024-11-18
confidence: high

patterns:
  - pattern: "DSC#####.JPG"
    description: "Standard JPEG naming (5 digits)"
    counter_range: "00001-99999"
    resets_on: ["memory card format"]
    models: "Alpha series, Cyber-shot"

  - pattern: "DSC#####.ARW"
    description: "RAW files"
    years: "2006-present"
    models: "Alpha series"

  - pattern: "_DSC####.ARW"
    description: "Alternative RAW naming (4 digits)"
    models: "Some older models"

  - pattern: "C####.MP4"
    description: "Video files (Cinema Line)"
    models: "FX3, FX6, FX9"

forensic_indicators:
  - indicator: "5-digit counter"
    meaning: "Standard Sony consumer/prosumer camera"
  - indicator: "4-digit counter with underscore"
    meaning: "Older Sony models"
  - indicator: "C prefix for video"
    meaning: "Cinema Line professional camera"

tags:
  - naming
  - forensics
---

# Sony File Naming Conventions

Sony uses distinctive 5-digit numbering that differs from most manufacturers' 4-digit patterns.

## Standard Pattern: DSC#####

Sony's signature 5-digit naming:
- Format: `DSC#####.EXT`
- Counter: 00001-99999
- Resets: When memory card is formatted
- Used by: Alpha series, Cyber-shot

### Why 5 Digits?

Sony chose a 5-digit counter to accommodate:
- Higher-capacity memory cards
- Extended shooting sessions
- Reduced need for folder increments

## JPEG Files

Standard JPEG naming:
- Pattern: `DSC#####.JPG`
- Range: 00001-99999
- Leading zeros: Always included

## RAW Files (ARW)

Sony's RAW format (Sony RAW, file extension ARW):

Current standard:
- Pattern: `DSC#####.ARW`
- Matches: JPEG numbering
- Introduced: 2006 with Alpha 100

Older format:
- Pattern: `_DSC####.ARW`
- 4 digits: Earlier convention
- Underscore prefix: Similar to Nikon

## Video Files

### Consumer/Prosumer Models
Standard naming continues:
- Pattern: `DSC#####.MP4` or `DSC#####.MTS` (AVCHD)

### Cinema Line
Professional video cameras use different scheme:
- Pattern: `C####.MP4` or `C####.MXF`
- 4 digits: Professional standard
- Models: FX3, FX6, FX9, VENICE

## Folder Structure Integration

Sony combines DCF structure with unique folder naming:
- Folder: `/100MSDCF/` (Memory Stick DCF)
- Legacy: "MS" references original Memory Stick format
- Modern: Used even with SD cards

## File Numbering Behavior

### Standard Sequence
- Increments with each shot
- Continues across power cycles
- Resets to 00001 on format

### Folder Creation
- New folder every 4,000 images (not 9,999 like Canon/Nikon)
- Folders: 100MSDCF, 101MSDCF, 102MSDCF...

## Identifying Sony Files

Definitive markers:
- 5-digit numbering (distinctive)
- DSC prefix (common with other brands)
- ARW extension (Sony-exclusive RAW format)
- Folder names containing "MSDCF"
