---
title: "Android Folder Conventions"
manufacturer: Android
device_type: phone, tablet
topic: folder-structures
last_verified: 2024-11-18
confidence: high

patterns:
  - pattern: "/DCIM/Camera/"
    description: "Camera default storage location"
    models: "Stock Android, many manufacturers"

  - pattern: "/DCIM/100ANDRO/"
    description: "Older default camera storage location"
    models: "Stock Android, many manufacturers"

  - pattern: "/Pictures/Screenshot/"
    description: "Screenshot storage location"
    models: "All Pixels"

tags:
  - foldering
  - mobile
  - android
---

Android phones may have multiple apps that can take pictures or videos. Each of these apps has its own folder(s) to store files, typically within one of the 3 media folders in the user's home folder.

- `/DCIM/` - primarily for camera-generated pictures and videos
- `/Movies/` - primarily for downloaded and edited videos
- `/Pictures/` - primarily for image editing and downloading apps

## Standard Folders: DCIM/Camera

The primary camera app stores images and video to folders named either `Camera` (newer phones) or `100ANDRO` (older phones)

```sh
├── DCIM/
│   └── Camera/
└── Pictures/
    └── Screenshots/
```

## Variations

### Variations on DCF-folder

Manufacturers may choose to use other variations on `100ANDRO` such as `100MEDIA` (generic) or `100LGDSC` (LG phones). Because Android files use timestamps, additional `101...`, `102...` folders are not necessary.

### Other Apps

Any other app that creates, downloads, or edits files may create one or more folders across the three folders.

```sh
├── DCIM/
│   ├── Blackmagic Camera/
│   └── Camera/
├── Movies/
│   ├── GoPro Exports/
│   ├── Instagram/
│   └── Messages/
└── Pictures/
    ├── Instagram/
    ├── Messages/
    └── Screenshots/
```

##

[Android Documentation](https://developer.android.com/reference/android/os/Environment#DIRECTORY_DCIM) only specifies the existence of DCIM folder as a "traditional" location.
