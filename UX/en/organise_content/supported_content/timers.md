# Timers

## Summary
* [Description](#description)
* [Content extension](#content-extension)
* [Create a stopwatch](#create-a-stopwatch)
* [Create a countdown](#create-a-countdown)
* [Create a timer](#create-a-timer)
* [Metadata available](#metadata-available)

## Description

This content type allows you to display a timer. It can be either a timer, or a stopwatch.

Here is a stopwatch :

![Stopwatch](../../img/content_stopwatch.jpg)

And here is a timer :

![Countdown](../../img/content_timer.jpg)

Timer duration can be changed by clicking on the pen icon :

![Countdown edition](../../img/content_timer_edit.jpg)

Once the timer has ticked, it blinks :

![Countdown blinks](../../img/content_timer_ticked.jpg)


## Content extension

To use a stopwatch, add the extension `.stopwatch` or `chrono` at the end of the name of your folder.
To use a countdown, add the extension `.countdown` or `minuteur` at the end of the name of your folder.
To use, either a stopwatch or a countdown, add the extension `.timer` or `horloge` at the end of the name of your folder.

## Create a stopwatch

1. In your environment folder, create a folder named `<name of your stopwatch>.stopwatch` (e.g. `My stopwatch.stopwatch`).
1. (Optional) You can change the preview of the Stopwatch. In your `.stopwatch` folder, put an image (`.jpg` or `.png`) named `_preview`. If you don't provide a `_preview`, the item will have a default preview (shown below).

## Create a countdown

1. In your environment folder, create a folder named `<(hours)h(minutes)m(seconds)s>.countdown` (e.g. `5m30s.countdown`). It will create a countdown initialized to last 5 minutes and 30 seconds.
1. (Optional) You can also define the duration of your timer inside a `_meta.txt` file. Add the value : 
   * `timer.duration = 5m30s` to create a timer that must last 5 minutes and 30 seconds.
   * `timer.format = HH:mm` combined with `timer.duration = 05:30` also create a timer that must last 5 minutes and 30 seconds.
1. (Optional) Your timer can be silent. Add the line `timer.silent = true` in a `_meta.txt` file.
1. (Optional) The ringtone can be customized. Add a file named `_alarm.mp3` or `_alarm.wav` in your `.countdown` folder.
1. (Optional) You can change the preview of the Timer. In your `.timer` folder, put an image (`.jpg` or `.png`) named `_preview`. If you don't provide a `_preview`, the item will have a default preview (shown below).

## Create a timer 

1. In your environment folder, create a folder named `<(hours)h(minutes)m(seconds)s>.timer` (e.g. `5m30s.tilmer`). It will create a countdown initialized to last 5 minutes and 30 seconds. You can also change it to a stopwatch by clicking on the stopwatch icon.

![Timer](../../img/content_timer2.jpg)

1. (Optional) You can also define the duration of your timer inside a `_meta.txt` file. Add the value : 
   * `timer.duration = 5m30s` to create a timer that must last 5 minutes and 30 seconds.
   * `timer.format = HH:mm` combined with `timer.duration = 05:30` also create a timer that must last 5 minutes and 30 seconds.
1. (Optional) Your timer can be silent. Add the line `timer.silent = true` in a `_meta.txt` file.
1. (Optional) The ringtone can be customized. Add a file named `_alarm.mp3` or `_alarm.wav` in your `.countdown` folder.
1. (Optional) You can change the preview of the Timer. In your `.timer` folder, put an image (`.jpg` or `.png`) named `_preview`. If you don't provide a `_preview`, the item will have a default preview (shown below).

![Timer preview](../../img/content_timer_preview.png)

## Metadata available

| Metadata Key                      | Type     | Default | Description |
|:--------------------------------- |:---------|:--------|:-|
| `timer.silent         `           | `bool`   | false   | sets the timer to silent mode |
| `timer.duration`                  | `text`   | 0       | sets the timer duration (e.g. 1h5m30s for 1 hour, 5 minutes and 30 seconds). If a `timer.format` is defined, it tries to parse the duration with the format. |
| `timer.format`                    | `text`   | -       | sets the format to use when parsing the duration (e.g. `hh:mm:ss`) |

[Access common metadatas](../advanced_setting.md#summary)

Next : [Slideshows (Compositeur Digital UX format)](slideshows.md)

[Back to Supported Content](index.md)
