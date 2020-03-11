# Advanced settings : metadata

You can modify a document's behavior or associated actions using specific parameters described in a file named `_meta.txt`.

To modify the behavior of a folder in the application, the meta file must be placed inside the targeted folder, and named `_meta.txt`.

To modify the behavior of a document in the application, the meta file must be named after the document's file name followed by the suffix `_meta` and the `txt` extension. It must be saved at the same location as the target document. 

> Example: for a file named `1 - image.jpg`, the corresponding meta file should to be named as follows : `1 - image_meta.txt`.

In the meta file, each line (called `meta`) shall describe a parameter using the following structure: `metaName = value`

A binary meta (true or false) is described as follows:  `metaName = true`. It's default value is `false`. The values `1` (true) and `0` (false) can also be used.

To apply a specific behavior to a set of documents, use the `*.` prefix on the description of the meta and save the meta file in the folder containing the set of targeted documents

> Example : `*.table.hideCommands = true`

## Summary 
* [Value types](#value-types)
* [Metadata supported](#metadata-supported)
* [Content specific metadata](#content-specific-metadata)
  * [Video and audio](#video-and-audio)
  * [Web](#web)
  * [Mortgage simulator](#mortgage-simulator)
  * [Savings simulator](#savings-simulator)
  * [3D objects](#3d-objects)
  * [Search interface](#search-interfaces)
* [Shared values](#shared-values)

## Value types

|Type         | Description | Examples|
|:------------|:------------|:--------|
| `text`      | a string of characters | `some text`, `My document` |
| `number`    | an integral or decimal number | `123`, `123.45` |
| `dimension` | a size in pixels or a percentage of the containing view | `400`, `75%` |
| `boolean`   | true or false | `true`/`false`, `1`/`0` |
| `color`     | hexadecimal color code or rgb code | `#AAAAAA`, `#f03b5e`, `112, 12, 67` |


## Metadata supported

| Metadata Key                      | Type         | Default   | Description |
|:--------------------------------- |:-------------|:----------|:-|
| `culture`                         | `text`       | unset     | indicates the language used in the universe. Supported values are `fr` or `en` |
| `canStick`                        | `boolean`    |false      | indicates that the object can be sticked like a note |
| `canWrite`                        | `boolean`    |false      | indicates that text can be typed on this object |
| `desiredHeight`                   | `dimension`  | 400       | sets the default height of the document |
| `desiredWidth`                    | `dimension`  | 400       | sets the default width of the document |
| `isPaper`                         | `boolean`    | false     | removes the background of the document's buttons (action and close buttons)|
| `hideBottomBarDots`               | `boolean`    | false     | hides the bottom bar button |
| `maxHeight`                       | `dimension`  | -         | sets the maximum height |
| `maxWidth`                        | `dimension`  | -         | sets the maximum width |
| `minHeight`                       | `dimension`  | -         | sets the minimum height |
| `minWidth`                        | `dimension`  | -         | sets the minimum width |
| `name`                            | `text`       | file name | change the displayed name of the document to "A name" (example) |
| `noChrome`                        | `boolean`    | false     | hides all the chrome buttons (close, menu), and the shadow under the document.|
| `orientation`                     | `number`     | 0         | rotates the document: `-90` to turn left, `90` to turn right or `180` to flip the document |
| `table.noClose`                   | `boolean`    | false     | prevents closing the document (close button disabled and throwing out of screen does not close) |
| `table.hideCommands`              | `boolean`    | false     | hides the control buttons of a document (previous/next page, video playback controls…) |
| `table.noRotate`                  | `boolean`    | false     | inhibits rotation for the document |
| `table.viewer`                    | `cdux` or `extern` | unset   | Using `cdux` it makes sure the `cdurl` link will be displayed inside Compositeur Digital UX. With `extern`, the document is opened using the native viewer. |
| `themeColor`                      | `color`      | -         | forces a theme color for the universe/element and its contents | 
| `table.showOnStart`               | `boolean`    | false     | open the document automatically when the universe is launched | 
| `hideLinkLabel`                   | `boolean`    | false     | hide the document name in the universe bottom bar |
| `table.alwaysBehind`              | `boolean`    | false     | force the document to stay under the others |
| `table.alwaysOnTop`               | `boolean`    | false     | force the document to stay on top of the others |

#### Menu actions

The default actions available in the document menu can be individually configured. Set the following parameters by replacing `<key>` with the action keys listed below. 
> Example: 
>
>`actions.saveas.disabled = true`  to hide the "Save as" action
>
>`actions.selection.location = shortcut` to give quick access to the selection action


| Metadata Key                      | Type         | Default   | Description |
|:--------------------------------- |:-------------|:----------|:-|
| `actions.disabled`                | `boolean`    | false     | hides the menu button entirely on a document. |
| `actions.<key>.disabled`   | `boolean`    | false     | hides the `<key>` action. |
| `actions.<key>.location`   | `menu` or `shortcut`       | menu      | defines if the `<key>` action should be available in the menu or as a shortcut. |

Configurable actions:

| Action key    | Description |
|:--------------|-------------|
|`capture`      | Create an image capture of the document | 
|`selection`    | Add or remove a document to/from the selection | 
|`duplicate`    | Duplicate the document | 
|`share`        | Share the document |
|`saveas`       | Save the document on the computer or on a removable device |
|`open`         | Open the document externally |


## Content specific metadata

### Video and audio

| Metadata Key                      | Type      | Default | Description |
|:--------------------------------- |:----------|:--------|:-|
| `video.autoplay`                  | `boolean` | true    | start playing video on display |
| `video.autoplay.delay`            | `number ` | 0       | delay autoplay by the number of seconds specified |
| `video.autoclose`                 | `boolean` | false   | close the video when playback reaches end |
| `video.autoclose.delay`           | `number ` | 0       | delay autoclose by the number of seconds specified |
| `video.mute`                      | `boolean` | false   | defines if a video is muted or not |
| `video.rewind`                    | `boolean` | false   | go back to the first frame when the video ends |
| `video.loop`                      | `boolean` | false   | replay from start when the video ends |
| `video.controls.alwaysvisible`    | `boolean` | false   | force the display of the video playback controls |
| `video.controls.hide`             | `boolean` | false   | hides the video playback controls permanently |

### Web

| Metadata Key                      | Type      | Default | Description |
|:--------------------------------- |:----------|:--------|:-|
| `web.manipulationMode`            | `number`  | 0       | If `1`, the user will have to enable navigation mode, then the view will behave like a browser. If `0`, the navigation mode will be reduced. |
| `web.showChrome`                  | `boolean` | false   | display a navigation bar at the top of the view |
| `web.viewport.width`              | `number`  | 1000    | Sets the default width of the page view |
| `web.viewport.height`             | `number`  | 800     | Sets the default height of the page view |

### Mortgage simulator

| Metadata Key                                 | Type     | Default            | Description |
|:-------------------------------------------- |:---------|:-------------------|:-|
| `simulator.additionalCostsRateDefaultValue`  | `number` | 0                  | sets the default value of the addtional costs rate |
| `simulator.additionalCostsRateLabel`         | `text`   | `Additional costs` | sets the label of the additional costs line | 
| `simulator.additionalCostsRateMinValue`      | `number` | 0                  | sets the min value for the additional costs rate |
| `simulator.additionalCostsRateMaxValue`      | `number` | 50                 | sets the max value for the additional costs rate |
| `simulator.additionalCostsRateTickFrequency` | `number` | 1                  | sets the interval between two values for the additional costs rate |
| `simulator.creditMaxValue`                   | `number` | 800000             | sets the maximum value of a loan |
| `simulator.creditTickFrequency`              | `number` | 5000               | sets the interval between two values for a loan |
| `simulator.creditDefaultValue`               | `number` | 300000             | sets the default loan value |
| `simulator.durationMinValue`                 | `number` | 5                  | sets the shortest duration of a loan |
| `simulator.durationMaxValue`                 | `number` | 30                 | sets the longest duration of a loan |
| `simulator.durationTickFrequency`            | `number` | 1                  | sets the interval between two values for a loan duration |
| `simulator.durationDefaultValue`             | `number` | 20                 | sets the default duration of a loan |

### Savings simulator

| Metadata Key                                 | Type     | Default            | Description |
|:-------------------------------------------- |:---------|:-------------------|:-|
| `simulator.depositFrequencyDefault`          | `text`   | `Month`            | sets the default value of the deposit frequency. It could be `Month`, `Quarter` or `Year` |
| `simulator.interestRateMinValue`             | `number` | 0                  | sets the min value for the interest rate |
| `simulator.interestRateMaxValue`             | `number` | 10                 | sets the max value for the interest rate |
| `simulator.interestRateDefaultValue`         | `number` | 2.75               | sets the default value for the interest rate |
| `simulator.regularDepositMinValue`           | `number` | 10                 | sets the minimum deposit value |
| `simulator.regularDepositMaxValue`           | `number` | 20000              | sets the maximum deposit value |
| `simulator.regularDepositTickFrequency`      | `number` | 100                | sets the interval between two values for a deposit |
| `simulator.savingsTermMinValue`              | `number` | 0                  | sets the shortest duration of a saving plan |
| `simulator.savingsTermMaxValue`              | `number` | 30                 | sets the longest duration of a saving plan |
| `simulator.savingsTermDefaultValue`          | `number` | 20                 | sets the default duration of a saving plan |
| `simulator.savingsTermTickFrequency`         | `number` | 1                  | sets the interval between two values for a saving plan duration |
| `simulator.startingDepositMinValue`          | `number` | 0                  | sets the min value for the starting deposit amount |
| `simulator.startingDepositMaxValue`          | `number` | 800000             | sets the max value for the starting deposit amount |
| `simulator.startingDepositTickFrequency`     | `number` | 5000               | sets the interval between two values for a starting deposit amount |

### 3D objects

| Metadata Key                      | Type     | Default | Description |
|:--------------------------------- |:---------|:--------|:-|
| `obj3D.backgroundcolor`           | `color`  | #dce1e1 | sets a solid background color |
| `obj3D.camera.h`                  | `number` | 0       | sets the default azimuth (horizontal rotation) for the camera position |
| `obj3D.camera.v`                  | `number` | 0       | sets the default pitch (vertical rotation) for the camera position |
| `obj3D.renderingmode`             | `text`   | Normal  | sets the rendering mode of the object. Supported modes are `Normal` (default mode), `Transparent` and `Wireframe`. |

### Search interfaces

| Metadata Key                      | Type     | Default | Description |
|:----------------------------------|:---------|:--------|:------------|
| `catalog.resultsMaxCount`         |`number`  | 40      | The maximum number of results wich can be viewed in the result page. |

## Shared values

Some values can be shared between different items, e.g. informations about a contact in a quiz or the result of a mortgage loan.

| Shared key                       | Type      | Description |
|:---------------------------------|:----------|:------------|
| `firstName`                      | `text`    | defines the first name of the current contact |
| `lastName`                       | `text`    | defines the last name of the current contact |
| `email`                          | `text`    | defines the email of the current contact |
| `phoneNumber`                    | `text`    | defines the phone number of the current contact |
| `organization`                   | `text`    | defines the organization of the current contact |
| `finance.budget`                 | `number`  | defines the amount of the mortgage loan of the current contact |



[Back to Organise Content](index.md)
