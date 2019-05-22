# Video

## Summary
* [Description](#description)
* [File extensions](#file-extensions)
* [Actions within Compositeur Digital UX](#actions-within-compositeur-digital-ux)
* [A/V Codecs](#av-codecs)
* [360° Videos](#360-videos)
* [Metadata available](#metadata-available)

## Description

Video are supported natively by Compositeur Digital UX.

![Video displayed within Compositeur Digital UX](../../img/content_video.JPG)

## File extensions 

Compositeur Digital UX supports `.avi`, `.flv`, `.m4v`, `.mov`, `.mp4`, `.mpeg`, `.mpg`, `.ts` and `.wmv` files.

## Actions within Compositeur Digital UX

Videos support the following action. To have a complete overview of each action, [see the section Actions](actions.md)

**Actions menu**

| Annotate | Capture  | Duplicate | Open in native app | Save as  | Selection | Share    | Loop     |
|:--------:|:--------:|:---------:|:------------------:|:--------:|:---------:|:--------:|:--------:|
| &#x2716; | &#x2714; | &#x2714;  | &#x2714;           | &#x2714; | &#x2714;  | &#x2714; | &#x2714; | 

**Interaction with the item**

| Video Controls |
|:--------------:|
| &#x2714;       | 

## A/V Codecs

A video file format can embed different coding/decoding standards. Those standards called “codecs” should be installed on your computer. K-Lite Codec Pack includes a wide variety of codecs. Please note that some uncommon codecs may not be supported within Compositeur Digital UX.

Our recommendation is to use WMV and MP4(H264) format for a safe use.

## 360° Videos

360° videos can be viewed with a controller that allows user to change the camera position. See the [section Panorama](panorama.md).

## Metadata available

| Metadata Key                      | Type      | Default | Description |
|:--------------------------------- |:----------|:--------|:-|
| `video.autoplay`                  | `boolean` | true    | start playing video on display |
| `video.autoplay.delay`            | `number ` | 0       | delay autoplay by the number of seconds specified |
| `video.autoclose`                 | `boolean` | false   | close the video when playback reaches end |
| `video.autoclose.delay`           | `number ` | 0       | delay autoclose by the number of seconds specified |
| `video.rewind`                    | `boolean` | false   | go back to the first frame when the video ends |
| `video.loop`                      | `boolean` | false   | replay from start when the video ends |
| `video.mute`                      | `boolean` | false   | force the video to be muted |
| `video.controls.alwaysvisible`    | `boolean` | false   | force the display of the video playback controls |

Next: [Audio (Compositeur Digital UX format)](audio.md)

[Back to Supported Content](index.md)
