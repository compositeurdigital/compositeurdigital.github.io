# Advanced configuration
## Metadata
You can modify a document's behavior or associated actions using specific parameters described in a file named `_meta.txt`.

To modify the behavior of a folder in the application, the meta file must be placed inside the targeted folder.

To modify the behavior of a document in the application, the meta file must be named after the document's file name followed by the suffix `_meta` and the `txt` extension. It must be saved at the same location as the target document. 

For example, for a file named `1 - image.jpg`, the corresponding meta file should to be named as follows : `1 - image_meta.txt`.

In the meta file, each line (called `meta`) shall describe a parameter using the following structure: `metaName = value`

A binary meta (true or false) is described as follows:  `metaName = true`. It's default value is `false`. The values `1` (true) and `0` (false) can also be used.

To apply a specific behavior to a set of documents, use the `*.` prefix on the description of the meta and save the meta file in the folder containing the set of targeted documents

Example : `*.table.hideCommands = true`


### Document configuration :
*Buttons :*
 - `table.hideCommands = true` hides the control buttons of a document. On a slideshow, the buttons Next, Previous and Slides will disappear. On a video, the buttons play/pause, mute and the progress bar will disappear.
 - `disablePrint = true` hides the print button
 - `disableAnnotation = true` hides the annotation button
 - `disableDuplicate = true` hides the duplicate button
 - `disableSendBehind = true` hides the "send to background" button

*Gestures :*
 - `table.noRotate = true` inhibits rotation for the document
 - `table.noScale = true` inhibits resizing for the document 
 - `table.noMove = true` inhibits all movements for the document (it will be opened in the middle of the screen)

*Size and displayed tags :*
 - `desiredHeight = 400` sets the default height of the document
 - `desiredWidth = 400` sets the default width of the document
 - `minHeight = 400` sets the minimum height
 - `minWidth = 400` sets the minimum width
 - `maxHeight = 400` sets the maximum height
 - `maxWidth = 400` sets the maximum width
 - `table.hideChrome = true` hides the shadow, the menu and the close button of a document
 - `table.alwaysBehind = true` forces the document to stay in background, behind the other documents
 - `name = toto` change the displayed name of a document to "toto" (example)
 - `hideLinkLabel = true` hides the name of the document
 - `orientation = 90` rotates the document using a specified value : `-90` to turn left, `90` to turn right or `180` to flip the document
 
### Environment parameters
*Theme color*
 - `themeColor = 9c211f` sets a specified value for the theme color. By default, the value is set the mean value of the color of the background

*Buttons :*
 - `disableGoBack = true` hides the back button
 - `disableReset = true` hides the reset button
 - `disableQuit = true` hides the quit button
 - `disableHelp = true` hides the help button
 - `disableContactUs = true` hides the contact button

*Favorites :*
 - `favorites.disableFastShare = true` hides the quick share button on all documents
 - `favorites.disableFavorites = true` disables the document basket/favorites feature.

*Paper notes:*
 - `paper.disableBlankSheet = true` hides the blanksheet creation button
 - `paper.disablePostIt = true` hides the note creation button

*Language:*
- `culture = en` in a file `_meta.txt` at the universe root force the UI language for this universe. (supported languages : en, fr). Note that default used language is based on your Windows language.

## Configuration files
Each parameter must be written using the following structure : 

`<param name="parameterName" value="parameterValue, secondOptionalValue, third, etc" />`

*App.xml*

 - `HomePage` by default : Table 
 - `DemoItems` address of the demo content (set by default to http://www.compositeurdigital.com/demo/contents/config.json ). It can also be the address of an embedded resource (ex : /Compositeur Digital;component/DemoContent.zip)
 - `ExplicitPlugins` : list of dll plugins to use
 - `ResetOnItemLoading` resets the environment on loading
 - `KioskMode` activates the kiosk mode : Hides all menus and the quit button (except if there are several environments)
 - `AutoResetInterval` in kiosk mode only : Duration in minutes between the last user action an automatic environment reload
 - `FavoritesDestinationPath` folder path to where favorites will be saved
 - `DisablePrint` disables print feature
 - `DisableAnnotation` disables annotations
 - `UseLegacyTouchEvents` if set to true, forces the use of Windows 7 touch events
 - `DisplayOnSecondaryScreen` if set to true, uses the secondary screen when available
 - `DisableFastShare` if set to true,  hides the quick share button on all documents
 - `DisableFavorites` disables the basket/favorites feature.
 - `DisableBlankSheet` hides the blanksheet creation 
 - `DisablePostIt` hides the note creation button
 - `CustomLogUIPath` path where UI logs (= analytics) will be stored. Copy previous logs saved in the default folder into this custom folder. Handle windows environment variables.
 - `HelpEmailAdress` custom support email adress
 - `AdditionalShareDestinations` adds new targets for share operations. Handles windows and Compositeur Digital environment variables. eg :
```xml
<param name="AdditionalShareDestinations">
 <shareDestinations>
  <shareDestination name="Universe" path="%UNIVERSE%\Exported Documents\" />
 </shareDestinations>
</param>
```

*Favorites.xml*
 - `FolderName` displayed name for the basket feature. By default, set to "basket"
 - `ContactInfos` contains the list of fields to be stored. By default set to :
 
 ```xml
    <contactInfos>
      <contactInfo key="true" label="name" />
      <contactInfo label="email" />
    </contactInfos>
```
 - `FavoritesDestinationPath` folder path to which favorites document will be saved
 - `DisableFastShare` hides the quick share button on all documents
 - `DisableFavorites` disable the document basket/favorites feature.

*Page.xml*
 - `DisableDuplicate` hides the duplicate button
 - `DisableSendBehind` hides the "send to background" button

*Common.xml*
 - `AdditionalRootItemsFolderPaths` list of addional directories in which the application will look for new environments 
 - `CacheDirectory` sets a specific folder to store cached files 
 
 ## Data exchanged between documents
 
 Some types of documents allow you to exchange data between documents  (e.g getting a value previously saved and modifying it)
 A keyword is used to operate this exchange of values. The following keys target attributes of the customer in the Profile view in the menu.
 Available keys are :
  - `firstName`
  - `lastName`
  - `email`
  - `phoneNumber`
  - `organization`
  - `finance.budget`

 ## Universes Categories

The universes can be sorted into categories by naming them with the pattern `category name, universe name` .
In the start page, you will then see buttons for each category that will display their inner universe on clic.
To customize categories look, you can add images named `category name_preview.jpg` or `category name_icon.jpg`in your `Compositeur Digital` folder.
In this same folder you can add a `_meta.txt` :
- `hidePageTitle = true` hides the `Compositeur Digital` title and logo
- `hideCategoriesTitle = true` hides the names of all categories



[Back to the menu](index.md)
