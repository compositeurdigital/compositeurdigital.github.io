# Audio

## Summary
* [Description](#description)
* [File extensions](#file-extensions)
* [Actions within Compositeur Digital UX](#actions-within-compositeur-digital-ux)
* [Metadata available](#metadata-available)

## Description

Audio files are supported natively by Compositeur Digital UX.

![Audio file displayed within Compositeur Digital UX](../../img/content_audio.JPG)

## File extensions 

Compositeur Digital UX supports `.mp3` files.

## Actions within Compositeur Digital UX

Audio player support the following action. To have a complete overview of each action, [see the section Actions](actions.md)

**Actions menu**

| Annotate | Capture  | Duplicate | Loop     |  Open in native app | Save as  | Selection | Share    | 
|:--------:|:--------:|:---------:|:--------:|:-------------------:|:--------:|:---------:|:--------:|
| &#x2716; | &#x2716; | &#x2714;  | &#x2714; | &#x2714;            | &#x2714; | &#x2714;  | &#x2714; | 

**Interaction with the item**

| Audio Controls |
|:--------------:|
| &#x2714;       | 


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

Next: [Guestbook (Compositeur Digital UX format)](guestbook.md)

[Back to Supported Content](index.md)
