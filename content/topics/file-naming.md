---
title: "File Naming Conventions"
type: topics
topic: file-naming
description: "Comprehensive comparison of file naming patterns across manufacturers"
---

# File Naming Conventions Across Manufacturers

Digital cameras have to give a unique name to every file created. There are a few ways to do this.

Most manufacturers begin file names with a hint about either:
- the content type
  - `IMG` or `P` for image
  - `MVI` for video
- the device
  - `DSC` for Digital Still Camera
  - `DSCF` for DSC Fujifilm
  - `PXL` for Google Pixel

After that, there may be delimiters, typically `_` or `-`, that increase the legiblity of the uniqueness part. And then, finally an extension that help identify the file format `.JPG`, `.CR2`, `.mp4`. There are many variations for the uniqueness portion.

At its simplest it's a counter, 0-padded to a set number of digits. In a 4-digit scheme, the first image can be given the name `IMG_0001.JPG`, then `IMG_0002.JPG`, and so forth. This is effective, but creates file management problems. When the counter hits the maximum number it resets, and the camera typically stores the next file in another folder.

A slightly more unique number is timestamp. At minimum, camera's will encode the UTC time down to the second using ISO 8601 order. A photo taken at 1 AM on January 2, 2023 in New York City, can be named `IMG_20230102_070000.JPG`. This introduces new complexity. What if the camera's clock is wrong?

Smart phone cameras may append additional abbreviations at the end of a file to indicate either a non-standard data stream in the file or the usage of computational techniques to create the stored image.
- `.MP.` for Google Motion Photos
- `.HDR.` for High Dynamic Range photos
- `.PORTRAIT.` for Portrait mode effects

## Comparison Table

{{< pattern-table topic="file-naming" >}}

## Detailed Information

Content below...