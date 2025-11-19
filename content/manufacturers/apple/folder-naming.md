---
title: "Apple Folder Conventions"
manufacturer: Apple
device_type: Phone, Tablet
topic: folder-structures
last_verified: 2024-11-18
confidence: low

patterns:
  - pattern: "/DCIM/###APPLE/"
    description: "DCF with Apple suffix"
    models: "All iDevices"
  - pattern: "/DCIM/###CLOUD/"
    description: "DCF with iCloud suffix"
    models: "All iDevices"

tags:
  - foldering
  - mobile
  - apple
---

Developers are instructed to use the PhotoKit API from to all image and videos managed by Photos. Within the iOS file system, images are stored according to a DCF folder system, although this is not exposed to most users.

## Standard Folders: DCIM/100APPLE and DCIM/100CLOUD

Files created on the device are stored to a `###APPLE` folder in accordance with DCF conventions. Once files have been uploaded to iCloud and deleted from the device, when they are downloaded again, they are stored in a `###CLOUD` folder.

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
