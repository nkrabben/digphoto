---
title: "Canon Folder Conventions"
manufacturer: Canon
device_type: Camera
topic: folder-structures
last_verified: 2024-11-18
confidence: low

patterns:
  - pattern: "/DCIM/100CANON/"
    description: "DCF with Canon suffix"
    models: "All still cameras"

tags:
  - foldering
  - canon
---

Canon uses a DCF file system. New folders are created

- Every 100 images
- At the start of every month
- Manually by the user

## Standard Folders: DCIM/100CANON

```sh
├── DCIM/
    ├── 100CANON/
    ├── 101CANON/
    └── ...
```

## Sources
