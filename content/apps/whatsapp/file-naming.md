---
title: "WhatsApp File Naming Conventions"
app: WhatsApp
app_type: Messaging
topic: file-naming
last_verified: 2024-11-18
confidence: medium

patterns:
  - pattern: "TYPE_yyyymmdd_WA####.EXT"
    description: "Sent and received images and video"
    counter_range: "0001-9999"

tags:
  - naming
  - mobile
  - app
---

WhatsApp file names are relative to the device sending or receiving the file name. If an image is sent from New York to Vietnam on 2019 August 1 at 11PM, the phone in New York will have `IMG_20190801_WA####.jpg` and the phone in Vietnam will store `IMG_20190802_WA####.jpg`.

The counter is also relative to the phone and spans all media types. If the image is the 30th WhatsApp file of the day for the phone in New York, it's `IMG_20190801_WA0029.jpg`. If it's the 4th WhatsApp file of the day for the phone in Vietnam, it's `IMG_20190802_WA0003.jpg`. And if the phone in Vietnam replies with a video voice note, it would be stored as `PTV_20190801_WA0030.mp4`

## Standard Pattern: IMG_yyyymmdd_WA####.EXT

- Format: `TYPE-yyyyMMdd-WA####.EXT`
- Type: varies on function in WhatsApp
- Datestamp: According to the date sent or received
- WA Counter: Resets daily across all images and videos
- Extension: varies on content type

### Images

#### Standard Photo

This includes any image that is created with the WhatsApp camera or attached by the WhatsApp image/video picker.

- Pattern: `IMG-yyyyMMdd-WA####.jpg`
- Example: `IMG-20190802-WA0000.jpg`

#### Attached Image

This includes any image that is selected from the general attachment picker.

- Pattern: `DOC-yyyyMMdd-WA####.ext`
- Example: `DOC-20190802-WA0001.jpg`

### Video

#### Standard Video

This includes any video that is created with the WhatsApp camera or attached by the WhatsApp image/video picker.

- Pattern: `VID-yyyyMMdd-WA####.mp4`
- Example: `VID-20190802-WA0003.mp4`

#### Attached Video

This includes any video that is selected from the general attachment picker.

- Pattern: `DOC-yyyyMMdd-WA####.ext`
- Example: `DOC-20190802-WA0004.mp4`

#### Video Note

This includes any video that created by long-pressing the camera button.

- Pattern: `PTV-yyyyMMdd-WA####.mp4`
- Example: `PTV-20190802-WA0005.mp4`

### Audio

#### Standard Audio

This includes any video that is created with the WhatsApp audio recorder.

- Pattern: `AUD-yyyyMMdd-WA####.opus`
- Example: `AUD-20190802-WA0006.opus`

#### Attached Audio

This includes any video that is selected from the general attachment picker.

- Pattern: `DOC-yyyyMMdd-WA####.ext`
- Example: `DOC-20190802-WA0007.m4a`

#### Audio Note

This includes any audio created by long-pressing the microphone button.

- Pattern: `PTT-yyyyMMdd-WA####.opus`
- Example: `PTT-20190802-WA0008.opus`
