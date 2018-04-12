# Advanced configuration

## Summary

* [Metadata](#metadata)
  * [Document configuration](#document-configuration)
    * [Buttons](#buttons)
    * [Gestures](#gestures)
    * [Size and displayed tags](#size-and-displayed-tags)
  * [Environment parameters](#environment-parameters)
    * [Theme color](#theme-color)
    * [Buttons](#buttons-1)
    * [Favorites](#favorites)
    * [Paper notes](#paper-notes)
    * [Language](#language)
* [Configuration files](#configuration-files)
  * [App.xml](#appxml)
  * [Favorites.xml](#favoritesxml)
  * [Page.xml](#pagexml)
  * [Common.xml](#commonxml)
* [Data exchanged between documents](#data-exchanged-between-documents)
* [Universes categories](#universes-categories)
    

## Metadata
You can modify a document's behavior or associated actions using specific parameters described in a file named `_meta.txt`.

To modify the behavior of a folder in the application, the meta file must be placed inside the targeted folder.

To modify the behavior of a document in the application, the meta file must be named after the document's file name followed by the suffix `_meta` and the `txt` extension. It must be saved at the same location as the target document. 

For example, for a file named `1 - image.jpg`, the corresponding meta file should to be named as follows : `1 - image_meta.txt`.

In the meta file, each line (called `meta`) shall describe a parameter using the following structure: `metaName = value`

A binary meta (true or false) is described as follows:  `metaName = true`. It's default value is `false`. The values `1` (true) and `0` (false) can also be used.

To apply a specific behavior to a set of documents, use the `*.` prefix on the description of the meta and save the meta file in the folder containing the set of targeted documents

Example : `*.table.hideCommands = true`


### Document configuration

#### Buttons

| Metadata key         | Value            | Description                                                                             |
|:---------------------|:----------------:|:----------------------------------------------------------------------------------------|
| `disableAnnotation`  | true/false - 1/0 | Hides the annotation button.                                                            |
| `disableDuplicate`   | "                | Hides the duplicate button.                                                             |
| `disablePrint`       | "                | Hides the print button.                                                                 |
| `disableSendBehind`  | "                | Hides the "send to background" button.                                                  |
| `table.hideCommands` |"                 | Hides the control buttons of a document. On a slideshow, the buttons Next, Previous and Slides will disappear. On a video, the buttons play/pause, mute and the progress bar will disappear. |


#### Gestures

| Metadata key         | Value            | Description                                                                             |
|:---------------------|:----------------:|:----------------------------------------------------------------------------------------|
| `table.noMove`       | true/false - 1/0 | Inhibits all movements for the document (it will be opened in the middle of the screen).|
| `table.noRotate`     | "                | Inhibits rotation for the document.                                                     |
| `table.noScale`      | "                | Inhibits resizing for the document.                                                     |

#### Size and displayed tags

| Metadata key         | Value                          | Description                                                               |
|:---------------------|:------------------------------:|:--------------------------------------------------------------------------|
| `desiredHeight`      | 400 (number) or 60% (percent*) | Sets the default height of the document.                                  |
| `desiredWidth`       | "                              | Sets the default width of the document.                                   |
| `hideLinkLabel`      | true/false - 1/0               | Hides the name of the document.                                           |
| `minHeight`          | 400 (number) or 60% (percent*) | Sets the minimum height of the document.                                  |
| `minWidth`           | "                              | Sets the minimum width of the document.                                   |
| `maxHeight`          | "                              | Sets the maximum height of the document.                                  |
| `maxWidth`           | "                              | Sets the maximum width of the document.                                   |
| `name`               | A name (characters)            | Changes the displayed name of a document to "A name" (example).           |
| `table.alwaysBehind` | true/false - 1/0               | Forces the document to stay in background, behind the other documents.    |
| `table.hideChrome`   | "                              | Hides the shadow, the menu and the close button of a document.            |
| `orientation`        | -90 or 90 or 180 (number)      | Rotates the document using a specified value : `-90` to turn left, `90` to turn right or `180` to flip the document. |

\* *60% means that the document will take 60% of the width (or height) of the screen.*

### Environment parameters

#### Theme color

| Metadata key | Value                      | Description                                                                           |
|:-------------|:--------------------------:|:--------------------------------------------------------------------------------------|
| `themeColor` | 9c211f (hexadecimal color) | Sets a specified value for the theme color. By default, the value computed is based on the color of the background (mean value). |

#### Buttons

| Metadata key       | Value            | Description                                                                               |
|:-------------------|:----------------:|:------------------------------------------------------------------------------------------|
| `disableContactUs` | true/false - 1/0 | Hides the contact button.                                                                 |
| `disableHelp`      | "                | Hides the help button.                                                                    |
| `disableGoBack`    | "                | Hides the back button.                                                                    |
| `disableQuit`      | "                | Hides the quit button.                                                                    |
| `disableReset`     | "                | Hides the reset button.                                                                   |


#### Favorites

| Metadata key                 | Value            | Description                                                                     |
|:-----------------------------|:----------------:|:--------------------------------------------------------------------------------|
| `favorites.disableFastShare` | true/false - 1/0 | Hides the quick share button on all documents.                                  |
| `favorites.disableFavorites` | "                | Disables the document basket/favorites feature.                                 |

#### Paper notes

| Metadata key              | Value            | Description                                                                        |
|:--------------------------|:----------------:|:-----------------------------------------------------------------------------------|
| `paper.disableBlankSheet` | true/false - 1/0 | Hides the blanksheet creation button.                                              |
| `paper.disablePostIt`     | "                | Hides the note creation button.                                                    |

#### Language 

| Metadata key       | Value            | Description                                                                               |
|:-------------------|:----------------:|:------------------------------------------------------------------------------------------|
| `culture`          | en / fr          | In a file `_meta.txt` at the universe root, it forces the UI language for this universe.  |   

*Note that the default used language is based on your Windows language.*

## Configuration files
Each parameter must be written using the following structure : 

`<param name="parameterName" value="parameterValue, secondOptionalValue, third, etc" />`

### App.xml

| Tag                           | Value               | Description                                                                |
|:------------------------------|:-------------------:|:---------------------------------------------------------------------------|
| `AdditionalShareDestinations` | xml code *          | Adds new targets for share operations. Handles windows and Compositeur Digital environment variables. |
| `CustomLogUIPath`             | `C:\MyPath\` (path) | Path where UI logs (= analytics) will be stored. Copy previous logs saved in the default folder into this custom folder. Handle windows environment variables. |
| `DemoItems`                   |  url, path          | Address of the demo content (default is `http://www.compositeurdigital.com/demo/contents/config.json`). It can also be the address of an embedded resource (ex : `/Compositeur Digital;component/DemoContent.zip`). |
| `DisableAnnotation`           | true / false - 1 /0 | If set to true, disables annotations.                                      |
| `DisableBlankSheet`           | "                   | If set to true, hides the blanksheet creation.                             |
| `DisableFastShare`            | "                   | If set to true,  hides the quick share button on all documents.            |
| `DisableFavorites`            | "                   | If set to true, disables the basket/favorites feature.                     |
| `DisplayOnSecondaryScreen`    | "                   | If set to true, uses the secondary screen when available.                  |
| `DisablePrint`                | "                   | If set to true, disables print feature.                                    |
| `DisablePostIt`               | "                   | If set to true, hides the note creation button.                            |
| `ExplicitPlugins`             | plugins             | List of dll plugins to use (ex : `CompositeurDigital.ShowUI.BoardPlugins.Wpf.dll`). |
| `FavoritesDestinationPath`    | `C:\MyPath\` (path) | Folder path to where favorites will be saved.                              |
| `HelpEmailAdress`             | email               | Custom support email adress.                                               |
| `HomePage`                    | Table               | Defines how the home page is structured.                                   |
| `KioskMode`                   | true / false - 1 /0 | If set to true, activates the kiosk mode. It hides all menus and the quit button (except if there are several environments). |
| `AutoResetInterval`           | 3 (minutes)         | In kiosk mode only, duration in minutes between the last user action an automatic environment reload. |
| `ResetOnItemLoading`          | true / false - 1 /0 | Resets the environment on loading.                                         |
| `UseLegacyTouchEvents`        | "                   | If set to true, forces the use of Windows 7 touch events.                  |

\* Example : 

```xml 
<param name="AdditionalShareDestinations">
  <shareDestinations>
    <shareDestination name="Universe" path="%UNIVERSE%\Exported Documents\" />
  </shareDestinations>
</param>
```

### Favorites.xml

| Tag                           | Value               | Description                                                                |
|:------------------------------|:-------------------:|:---------------------------------------------------------------------------|
| `ContactInfos`                | xml code *          | Contains the list of fields to be stored.                                  |
| `DisableFastShare`            | true / false - 1 /0 | Hides the quick share button on all documents.                             |
| `DisableFavorites`            | "                   | Disables the document basket/favorites feature.                            |
| `FavoritesDestinationPath`    | `C:\MyPath\` (path) | Folder path to which favorites document will be saved.                     |
| `FolderName`                  | characters          | Displayed name for the basket feature. By default, set to "basket".        |
 
 \* Example :
 
 ```xml
    <contactInfos>
      <contactInfo key="true" label="name" />
      <contactInfo label="email" />
    </contactInfos>
```


### Page.xml

| Tag                           | Value               | Description                                                                |
|:------------------------------|:-------------------:|:---------------------------------------------------------------------------|
| `DisableDuplicate`            | true / false - 1 /0 | Hides the duplicate button on all documents.                               |
| `DisableSendBehind`           | "                   | Hides the `Send to background` button on all documents.                    |

### Common.xml


| Tag                              | Value               | Description                                                             |
|:---------------------------------|:-------------------:|:------------------------------------------------------------------------|
| `AdditionalRootItemsFolderPaths` | path                | List of addional directories in which the application will look for new environments. |
| `CacheDirectory`                 | "                   | Sets a specific folder to store cached files.                           |


## Data exchanged between documents
 
 Some types of documents allow you to exchange data between documents  (e.g getting a value previously saved and modifying it).
 A keyword is used to operate this exchange of values. The following keys target attributes of the customer in the `Profile` view in the menu.
 Available keys are :
  - `firstName`
  - `lastName`
  - `email`
  - `phoneNumber`
  - `organization`
  - `finance.budget`

## Universes categories

The universes can be sorted into categories by naming them with the pattern `category name, universe name` .
In the start page, you will then see buttons for each category that will display their inner universe on clic.
To customize categories look, you can add images named `category name_preview.jpg` or `category name_icon.jpg`in your `Compositeur Digital` folder.
In this same folder you can add a `_meta.txt` :

| Metadata key              | Value            | Description                                                                        |
|:--------------------------|:----------------:|:-----------------------------------------------------------------------------------|
| `hideCategoriesTitle`     | true/false - 1/0 | Hides the names of all categories.                                                 |
| `hidePageTitle`           | "                | Hides the `Compositeur Digital` title and logo.                                    |


[Back to the menu](index.md)
