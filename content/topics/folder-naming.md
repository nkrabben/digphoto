---
title: "Folder Naming Conventions"
type: topics
topic: folder-structures
description: "Comprehensive comparison of folder naming patterns across manufacturers"
---

Most cameras follow the Design rule for Camera File (DCF) system first published in 1998. A root parent-folder named `/DCIM/` holds 8-character, all-caps child folders named `/###CANON/` or `/###APPLE/`, and the child folders hold the media. Even iOS, which hides its folder structure from the user uses this convention. Higher-end cameras may use a non-DCF structure like BPAV to store videos.

Apps that are able to create, send, or receive media, follow their own conventions, sometimes platform-specific. Because iOS forces apps to store files in sandboxed application folders which are difficult for a a user to view, these are mostly undocumented here. Android apps may use one or more locations that may or may not be accessible outside of the application. Apps with a privacy need have generally moved towards less-accessible parts of the hierarchy. This change is documented when possible.

## Comparison Table

{{< device-table topic="folder-structures" >}}

{{< app-table topic="folder-structures" >}}

## Detailed Information

Before a file is stored, it needs a place to be stored. Generally, this is a digital storage device like an SD card, an SSD, or even a floppy disk, formatted according to some standard like FAT32 that supports folders. These folders can be provenance for the origin of the file.

The existence of a `/DCIM/` parent folder dates the images to after the publication of the 2003 DCF standard. That standard was created to promote interoperabitliy between cameras, photo kiosks, printers, and other devices. Within a DCF `/DCIM/` folder a manufacturer can create child folders with up to 9999 media files. These child folders tend to include the manufacturers name (`/100CANON/`, `/100_FUJI/`, `/100GOPRO/`, etc).

Video cameras did not have the same need for multi-device interoperability. Multiple structures developed, sometimes shared between manufacturuers. Some manufacturers, like Sony, created competing structures for different camera lines.

Many manufactures deviated from the requirements of DCF, but the generally kept the form. The rise of the smartphones and cloud storage have created an alternate method. Folder structures encourage users to organize files into easily summarized groups such as events or months. Cloud storage and phone apps encourage users to view their collection as a searchable hoard of images from all sources instead of a maze of folders. Even if the phone is still using DCF-like foldering, the user is discouraged or blocked from seeing that.

1. Pre-2003: Manufacturer Chaos
   1. Every manufacturer does what they want
   2. Filesystem constraints (FAT16/32) influence early decisions
2. 2003: DCF Standard
   1. DCIM folder standardization
   2. Why: interoperability with printers, kiosks, computers
   3. Limitations built in (FAT32 assumptions)
3. Camera Manufacturers (2003-present)
   1. Adopt DCF core, add manufacturer-specific extensions
   2. Dual-card behaviors create multiple structures
   3. Video chaptering due to FAT32 4GB limit

4. Professional Video (divergence)
   1. BPAV, P2, XDCAM structures
   2. Sometimes layered on DCF, sometimes replace it
   3. MXF-based workflows with XML metadata
5. Mobile Devices (2007-present)
   1. Phones follow DCF but add:
   2. Screenshots, screen recordings
   3. App-specific folders
   4. Cloud integration folders
   5. Internal vs. external folder views differ
6. Action Cameras & Drones (2010s-present)
   1. New structures for telemetry (SRT files, LRV proxies)
   2. 360° cameras add stitching considerations
   3. GPS/sensor data integration

7. Computer Import Software (major reorganizer)
   1. Date-based hierarchies replace camera folders
   2. Software-managed libraries (Photos, Lightroom)
   3. Many donated collections arrive in this state
8. Cloud Storage Era (2010s-present)
   1. Flattening of folder structures
   2. Metadata-based organization replaces folders
   3. Download/export creates new artificial structures
9. Filesystem Evolution Impact
    1. FAT32 → exFAT changes design decisions
    2. Larger files possible, different folder strategies
    3. Platform differences (iOS APFS, Android ext4/F2FS)
10. Ecosystem Files (often overlooked)
    1. Sidecar files (.XMP, .AAE)
    2. System files (Thumbs.db, .DS_Store)
    3. Metadata databases
    4. Often separated from originals in transfers
