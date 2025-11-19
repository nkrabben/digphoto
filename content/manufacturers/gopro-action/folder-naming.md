---
title: "GoPro Folder Conventions"
manufacturer: GoPro
device_type: Action
topic: folder-structures
last_verified: 2024-11-19
confidence: low

patterns:
  - pattern: "/DCIM/###GOPRO/"
    description: "DCF with GOPRO suffix"
    models: "All GoPros"

tags:
  - foldering
  - gopro
---

GoPro adheres to most of DCF. Video files are stored in the same folder as well as GoPro's video thumbnail format LRV.

## Standard Folders: DCIM/Camera

```sh
├── DCIM/
│   └── 100GOPRO/
│       ├── GH010001.MP4
│       ├── GL010001.LRV
│       └── GH010001.THM
```
