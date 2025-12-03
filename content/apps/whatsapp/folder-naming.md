---
title: "WhatsApp Folder Conventions"
app: WhatsApp
app_type: Messaging
topic: folder-structures
last_verified: 2024-12-2
confidence: high

patterns:
  - pattern: "WhatsApp/Media/WhatsApp {Type}/"
    description: "Location for received and copied files of a type"
    platform: Android

  - pattern: "Media/{Phone Number}"
    description: "Location for files from one conversation"
    platform: iOS

tags:
  - foldering
  - mobile
  - app
  - android
  - iOS
---

## Android

Originally in `/sdcard/WhatsApp/Media`, media storage was moved to `/sdcard/Android/media/com.WhatsApp/WhatsApp/Media` with Android 11's scoped storage update.

### Standard Folders: WhatsApp/Media/WhatsApp {Type}/(Sent|Private)

All files sent and received via WhatsApp are foldered by the following schema:

- Type: Audio, AI Media, Animated Gifs, Audio, Documents, Images, Stickers, Video, Video Notes, Voice Notes
- `Sent`: For the further processed versions of files sent by the user
- `Private`: For any files the user doesn't want discoverable by other applications, configured by conversation.

```sh
└── Media/
    ├── WhatsApp Audio
    │   ├── Private
    │   └── Sent
    ├── WhatsApp Documents
    │   ├── Private
    │   └── Sent
    ├── WhatsApp Images
    │   ├── Private
    │   └── Sent
    ├── WhatsApp Video
    │   ├── Private
    │   └── Sent
    └── WhatsApp Voice Notes
        ├── 201701
        ├── 201705
        └── ...
```

As WhatsApp adds more categories of files, they create additional folders.

Files created by another app are copied to `WhatsApp {Type}` with the WhatsApp file naming convention, then a compressed version is created for sending, and stored in `WhatsApp {Type}/Sent` with a counter incremented by 1. When files are created within WhatsApp with the camera, audio recorder, or editor functions, the file is save directly to `WhatsApp {Type}/Sent`.

```sh
└── WhatsApp Images
    ├── IMG-20150325-WA0000.jpg # Copy of original image
    └── Sent
        ├── IMG-20150325-WA0001.jpg # Compressed version of WA0000
        └── IMG-20150325-WA0003.jpg # Image from WhatsApp Camera
```

#### Images

Images sent as images are stored in `WhatsApp Images` and `WhatsApp Images/Sent`. Images attached as a generic file are stored in `WhatsApp Documents`.

#### Video

Videos sent as videos are stored in `WhatsApp Video` and `WhatsApp Video/Sent`. Videos attached as a generic file are stored in `WhatsApp Documents`.

Video recorded by holding the camera button in WhatsApp are stored in `WhatsApp Video Notes`. Within the folder, files are stored in weekly folders named `yyyyww`.

```sh
└── WhatsApp Video Notes
    ├── 202301 # First week of January
    ├── 202305 # Skips to a week in February
    └── ...
```

#### Audio

Audio sent as audio is stored in `WhatsApp Audio` and `WhatsApp Audio/Sent`. Audio attached as a generic file are stored in `WhatsApp Documents`.

Audio recorded by holding the microphone in WhatsApp are stored in `WhatsApp Voice Notes`. Within the folder, files are stored in weekly folders named `yyyyww`.

```sh
└── WhatsApp Voice Notes
    ├── 201701 # First week of January
    ├── 201705 # Skips to a week in February
    └ ...
```

## iOS

All app data is stored in a directory with `/private/var/mobile/`, previous conventions have included `/private/var/mobile/Applications/group.net.whatsapp.WhatsApp.shared` and `/private/var/mobile/Containers/Shared/AppGroup/{GUID}/`.

### Standard Folders

All file types for each conversation are stored in a single folder.

```sh
└── Media/
    ├── {phone number}@s.whatsapp.net/
    │   └── a/         # probably first character of hash
    │       └── 0/     # probably second character of a hash
    ├── {phone number}@s.whatsapp.net/
    ├── ...
```
