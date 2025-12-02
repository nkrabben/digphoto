---
title: "WhatsApp Folder Conventions"
app: WhatsApp
app_type: Messaging
topic: folder-structures
last_verified: 2024-12-2
confidence: high

patterns:
  - pattern: "WhatsApp/Media/WhatsApp {Type}/"
    description: "Location for received files of a type"
    model: Android

  - pattern: "WhatsApp/Media/WhatsApp {Type}/Sent"
    description: "Location for sent files of a type"
    model: Android

  - pattern: "WhatsApp/Media/WhatsApp {Type}/Private"
    description: "Location for received files of a type the user doesn't want available to other apps"
    model: Android

tags:
  - foldering
  - mobile
  - android
---

The WhatsApp folder has migrated to less visible location. Originally in the user's home directory, since 2021 it can be  `/home/Android/media/com.WhatsApp`

## Standard Folders: WhatsApp/Media/WhatsApp {Type}/(Sent|Private)

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

When audio or video is sent, an original version is stored in the parent folder, and a further compressed version is stored in the `Sent` folder with a counter incremented by one.

### Images

Images created by the WhatsApp camera or attached by the image option are store in `WhatsApp Images`. Images attached as a generic file are stored in `WhatsApp Documents`.

### Video

Videos created with the WhatsApp camera or attached by the image option are store in `WhatsApp Video`. Videos attached as a generic file are stored in `WhatsApp Documents`.

Video recorded by holding the camera button in WhatsApp are stored in `WhatsApp Video Notes`. Within the folder, files are stored in weekly folders named `yyyyww`.

```sh
└── WhatsApp Video Notes
    ├── 202301 # First week of January
    ├── 202305 # Skips to a week in February
    └── ...
```

### Audio

Audio created by tapping the microphone in WhatsApp are stored in `WhatsApp Audio`. Audio attached as a generic file are stored in `WhatsApp Documents`.

Audio recorded by holding the microphone in WhatsApp are stored in `WhatsApp Voice Notes`. Within the folder, files are stored in weekly folders named `yyyyww`.

```sh
└── WhatsApp Voice Notes
    ├── 201701 # First week of January
    ├── 201705 # Skips to a week in February
    └ ...
```
