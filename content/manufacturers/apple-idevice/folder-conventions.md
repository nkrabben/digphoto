---
title: "Apple Folder Conventions"
manufacturer: Apple
device_type: iPhone, iPad
topic: folder-structures
last_verified: 2024-11-18
confidence: low

patterns:
  - pattern: "/DCIM/###APPLE/"
    description: "Camera storage location"
    models: "All iDevices"
  - pattern: "/DCIM/###CLOUD/"
    description: "iCloud download location"
    models: "All iDevices"

tags:
  - foldering
  - mobile
  - apple
---

Developers are instructed to use the PhotoKit API from to all image and videos managed by Photos. Within the iOS file system, images are stored according to a DCF folder system, although this is not exposed to most users.

## Standard Folders: DCIM/100APPLE

```sh
├── DCIM/
    ├── 100APPLE/
    ├── 101APPLE/  # after 1,000 images and videos
    ├── ...
    ├── 100CLOUD/  # for cloud-stored files that have been downloaded
    ├── 101CLOUD/
    └── ...
```

## Sources

[PhotoKit API](https://developer.apple.com/documentation/photokit)
