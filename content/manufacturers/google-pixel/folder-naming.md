---
title: "Google Pixel Folder Conventions"
manufacturer: Google
device_type: Phone
topic: folder-structures
last_verified: 2024-11-19
confidence: high

patterns:
  - pattern: "/DCIM/Camera/"
    description: "Camera default storage location"
    models: "All Pixels"

  - pattern: "/Pictures/Screenshot/"
    description: "Screenshot storage location"
    models: "All Pixels"

tags:
  - foldering
  - mobile
  - android
---

Google Pixels follow the default Android folder practice.

## Standard Folders: DCIM/Camera

```sh
├── DCIM/
│   └── Camera/
└── Pictures/
    └── Screenshots/
```
