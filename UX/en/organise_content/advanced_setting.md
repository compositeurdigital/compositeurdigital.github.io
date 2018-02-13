# Documentation

## Advanced settings : Metadata

You can modify a document's behavior or associated actions using specific parameters described in a file named `_meta.txt`.

To modify the behavior of a folder in the application, the meta file must be placed inside the targeted folder, and must be named `_meta.txt`.

If you want to modify the behaviour of a file in the application, the meta file must be named after the document's file name, followed by the suffix `_meta` and the `.txt` extension. It must be saved at the same location as the target document. 

> E.g. for a file named `1 - image.jpg`, the corresponding meta file should be named as follow : `1 - image_meta.txt`.

In the meta file, each line (called `meta`) shall describe a parameter using the following structure: `metaName = value`

A binary meta (true or false) is described as follows:  `metaName = true`. Its default value is `false`. The values `1` (true) and `0` (false) can also be used.

To apply a specific behavior to a set of documents, use the `*.` prefix on the description of the meta and save the meta file in the folder containing the set of targeted documents.

> Example : `*.table.hideCommands = true`, will hide the navigation buttons (i.e. `<` and `>`) for all the items belonging to the folder.

### Document configuration :

*Buttons :*
 - `table.hideCommands = true` hides the control buttons of a document. On a slideshow, the buttons `<`, `>` will disappear.

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
 - `orientation = 90` rotates the document using a specified value : `-90` to turn left, `90` to turn right or `180` to flip the document
 - `isPaper = false` buttons of the document (action button, close button) will not have any background if this value is set to true. The document will have the same look as a blanksheet or a note.
 
*Mortgage Simulator*
- `simulator.creditMaxValue = 800000` sets the limits for a loan
- `simulator.creditTickFrequency = 5000` sets the interval between two values when computing a loan 
- `simulator.creditDefaultValue = 300000` sets the starting value of a loan
- `simulator.durationMinValue = 5` sets the shortest duration of a loan
- `simulator.durationMaxValue = 30` sets the longest duration of a loan
- `simulator.durationTickFrequency = 1` sets the interval betweeb two values when computing loan duration
- `simulator.durationDefaultValue = 25` sets the default duration of a loan

*Video*
- `video.loop = false` defines if the video will be automatically restarted at the beginning when the video is over.


[Back to the menu](index.md)
