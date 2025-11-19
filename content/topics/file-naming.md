---
title: "File Naming Conventions"
type: topics
topic: file-naming
description: "Comprehensive comparison of file naming patterns across manufacturers"
---

# File Naming Conventions Across Manufacturers

In 1998, DCF introduced a very durable file naming schema, 4 characters for an identifier, 4 characters for a counter, 4 characters for the extension. The only allowed characters are `A-Z`, `0-9`, and a `.`. The schema balanced file-system compatibility requirements with corporate branding opportunities and has been followed by most camera manufacturers for nearly 30 years.

The most DCF file name is the most generic, `IMG_####.JPG`, used by Apple and Canon, as well as toy cameras. Other manufacturers use the first 4 characters as a branding exercise: `DSCF` for Digital Still Camera Fuji or `GOPR` for GoPro images.

The second component is a counter, 0-padded to a set number of digits. The first image can be given the name `IMG_0001.JPG`, then `IMG_0002.JPG`, and so forth. This is effective, but creates file management problems. When the counter hits the maximum number it resets, and the camera typically stores the next file in another folder.

Some manufacturers expand the 4-digit counter to 5-, 6-, or 7- digits. This isn't quite in the spirit of DCF, but it allows users to take many more pictures with a camera without every worrying about filename collisions. Olympus uses `P#######.JPG` and Leica uses `L#######.JPG`. Some manufacturers create sub-counters for issues with large video files or burst images. GoPro uses `GHXX####.MP4` where the #### is a counter of videos and the XX is a counter for chapter files.

The biggest divergence in this space has been Google, which completely abandoned the counter component in favor of timestamps. Google via Android has promulgated filenames like `IMG_YYYYMMDD_HHMMSS.jpg`. This solves the filename collision problem and introduces a potential confusion. Depending on the manufacturer or app, the timestamp may be in the user's local timezone or in the UTC timezone. Generally there is richer metadata embedded within the file that removes the confusion, but that's not always the case or it could be removed by another app.

There has been further divergence from DCF. Some manufacturers now prefer lower-case extensions or 4-character extensions like Apple's `.heic`. Google tends to highlight special camera modes by appending codes on the filename like `.PORTRAIT.jpg`.

Messaging apps deal with this variety in one of two ways. They retain the filenames as-is, or they assign new filenames like WhatsApp's `IMG_yyyyMMdd_WA###.jpg`.

## Comparison Table

{{< pattern-table topic="file-naming" >}}

{{< app-table topic="file-naming" >}}
