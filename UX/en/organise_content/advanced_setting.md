# Advanced settings : metadata

You can modify a document's behavior or associated actions using specific parameters described in a file named `_meta.txt`.

To modify the behavior of a folder, the meta file must be placed inside the targeted folder, and named `_meta.txt`.

To modify the behavior of a document, the meta file must be named after the document's file name followed by the suffix `_meta` and the `txt` extension. It must be saved at the same location as the target document. 

> Example: for a file named `1 - image.jpg`, the corresponding meta file should to be named as follows : `1 - image_meta.txt`.

In the meta file, each line (called `meta`) shall describe a parameter using the following structure: `metaName = value`

A binary value (true or false) is described as follows:  `metaName = true`. Its default value is `false`. The values `1` (true) and `0` (false) can also be used.

To apply a specific behavior to a set of documents, use the `*.` prefix on the parameter and save the meta file in the folder containing the set of targeted documents

> Example : `*.table.hideCommands = true`

## Summary 
* [Value types](#value-types)
* [Metadata supported](#metadata-supported)
  * [Inking](#inking)
  * [Menu actions](#menu-actions)
  * [Configurable actions](#configurable-actions)
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
| `culture`                         | `text`       | -         | indicates the language used in the universe. Supported values are `fr` or `en` |
| `canStick`                        | `boolean`    | false     | indicates that the object can be sticked like a note |
| `canWrite`                        | `boolean`    | false     | indicates that text can be typed on this object |
| `desiredHeight`                   | `dimension`  | 400       | sets the default height of the document |
| `desiredWidth`                    | `dimension`  | 400       | sets the default width of the document |
| `desiredPosition(.x|.y)`          | `position`   | auto      | controls where the documment appears on screen. Set both `desiredPosition.x` and `desiredPosition.y` to a relative value (eg `desiredPosition.x=50%`) or use a predefined value `center`, `top`,`left`, `right`,`bottom`, `topleft`, `topright`, `bottomleft`, `bottomright` (eg `desiredPosition=center`) |
| `isPaper`                         | `boolean`    | false     | removes the background of the document's buttons (action and close buttons)|
| `hideBottomBarDots`               | `boolean`    | false     | hides the bottom bar button when collapsed |
| `hideBottomBar`                   | `boolean`    | false     | hides the bottom bar completely when collapsed |
| `maxHeight`                       | `dimension`  | -         | sets the maximum height |
| `maxWidth`                        | `dimension`  | -         | sets the maximum width |
| `minHeight`                       | `dimension`  | -         | sets the minimum height |
| `minWidth`                        | `dimension`  | -         | sets the minimum width |
| `name`                            | `text`       | file name | change the displayed name of the document to "A name" (example) |
| `hidden`                          | `boolean`    | false     | hides the item from the main bar or folder views |
| `noChromeButtons`                 | `boolean`    | false     | hides all the chrome buttons (close, menu).|
| `noChromeShadow`                  | `boolean`    | false     | hides the shadow under the document.|
| `noChrome`                        | `boolean`    | false     | hides all the chrome buttons (close, menu), and the shadow under the document.|
| `orientation`                     | `number`     | 0         | rotates the document: `-90` to turn left, `90` to turn right or `180` to flip the document |
| `table.noClose`                   | `boolean`    | false     | prevents closing the document (close button disabled and throwing out of screen does not close) |
| `table.hideCommands`              | `boolean`    | false     | hides the control buttons of a document (previous/next page, video playback controls…) |
| `table.noRotate`                  | `boolean`    | false     | inhibits rotation for the document |
| `table.viewer`                    | `cdux` or `extern` | unset   | Using `cdux` it makes sure the `cdurl` link will be displayed inside Compositeur Digital UX. With `extern`, the document is opened using the native viewer. |
| `themeColor`                      | `color`      | -         | forces a theme color for the universe/element and its contents | 
| `table.showOnStart`               | `boolean`    | false     | open the document automatically when the universe is launched | 
| `noHistory`                       | `boolean`    | false     | prevent the document from going to the recycle bin when closed | 
| `hideLinkLabel`                   | `boolean`    | false     | hide the document name in the universe bottom bar |
| `hideLinkTypeIcon`                | `boolean`    | false     | hide the document type icon in folder views |
| `table.alwaysBehind`              | `boolean`    | false     | force the document to stay under the others |
| `table.alwaysOnTop`               | `boolean`    | false     | force the document to stay on top of the others |
| `toolbox.startOpened`             | `boolean`    | false     | the toolbox category will be opened when accessed from the sidebar |

### Inking

Set the default ink color and size for an universe with the follwing parameters:

| Metadata Key      | Type         | Default   | Description |
|:----------------- |:-------------|:----------|:-|
| `ink.color`       | `red|orange|yellow|green|turquoise|blue|pink|violet|black|white` | black | sets the default pen color |
| `ink.penName`     | `fine|thick|marker` | fine    | set the default pen size |

### Menu actions

The default actions available in the document menu can be individually configured. Set the following parameters by replacing `<key>` with the action keys listed below. 
> Example: 
>
>`actions.saveas.disabled = true`  to hide the "Save as" action
>
>`actions.selection.location = shortcut` to give quick access to the selection action

| Metadata Key                      | Type                  | Default   | Description                                                                     |
|:----------------------------------|:----------------------|:----------|:--------------------------------------------------------------------------------|
| `actions.disabled`                | `boolean`             | false     | hides the menu button entirely on a document.                                   |
| `actions.<key>.disabled`          | `boolean`             | false     | hides the `<key>` action.                                                       |
| `actions.<key>.location`          | `menu` or `shortcut`  | menu      | defines if the `<key>` action should be available in the menu or as a shortcut. |

### Configurable actions:

| Action key    | Description |
|:--------------|-------------|
|`capture`      | Create an image capture of the document | 
|`selection`    | Add or remove a document to/from the selection | 
|`duplicate`    | Duplicate the document | 
|`share`        | Share the document |
|`saveas`       | Save the document on the computer or on a removable device |
|`open`         | Open the document externally |

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
