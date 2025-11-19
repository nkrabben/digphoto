---
title: "Sony Camera Folder Conventions"
manufacturer: Sony
device_type: Camera
topic: folder-structures
last_verified: 2024-11-18
confidence: low

patterns:
  - pattern: "/DCIM/100MSDCF/"
    description: "DCF with Sony suffix"
    models: "All still cameras"

tags:
  - foldering
  - sony
---

Sony uses a DCF file system. New folders are created

- Every 100 images
- At the start of every month
- Manually by the user

MSDCF stands for MemoryStick DCF, Sony's own memory card format.

## Standard Folders: DCIM/100CANON

```sh
├── DCIM/
    ├── 100MSDCF/
    ├── 101MSDCF/
    └── ...
```

## Sources

