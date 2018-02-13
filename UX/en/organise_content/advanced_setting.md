# Documentation

## Advanced setting

You can modify a document's behavior or associated actions using specific parameters described in a file named `_meta.txt`.

To modify the behavior of a folder in the application, the meta file must be placed inside the targeted folder, and named `_meta.txt`.

To modify the behavior of a document in the application, the meta file must be named after the document's file name followed by the suffix `_meta` and the `txt` extension. It must be saved at the same location as the target document. 

> Example: for a file named `1 - image.jpg`, the corresponding meta file should to be named as follows : `1 - image_meta.txt`.

In the meta file, each line (called `meta`) shall describe a parameter using the following structure: `metaName = value`

A binary meta (true or false) is described as follows:  `metaName = true`. It's default value is `false`. The values `1` (true) and `0` (false) can also be used.

To apply a specific behavior to a set of documents, use the `*.` prefix on the description of the meta and save the meta file in the folder containing the set of targeted documents

> Example : `*.table.hideCommands = true`


### Document configuration :
*Buttons :*
 - `table.hideCommands = true` hides the control buttons of a document. On a slideshow, the buttons `<` and `>` will disappear.

*Gestures :*
 - `table.noRotate = true` inhibits rotation for the document
 - `table.noScale = true` inhibits resizing for the document 
 - `table.noMove = true` inhibits all movements for the document (it will be opened in the middle of the screen)
 
 *Mortgage Simulator :*
- `simulator.creditMaxValue = 800000` sets the maximum value of a loan
- `simulator.creditTickFrequency = 5000` sets the interval between two values for a loan
- `simulator.creditDefaultValue = 3000000` sets the default loan value
- `simulator.durationMinValue = 5` sets the shortest duration of a loan
- `simulator.durationMaxValue = 30` sets the longest duration of a loan
- `simulator.durationTickFrequency = 1` sets the interval between two values for a loan duration
- `simulator.durationDefaultValue = 20` sets the default duration of a loan

*Size and displayed tags :*
 - `desiredHeight = 400` sets the default height of the document
 - `desiredWidth = 400` sets the default width of the document
 - `maxHeight = 400` sets the maximum height
 - `maxWidth = 400` sets the maximum width
 - `minHeight = 400` sets the minimum height
 - `minWidth = 400` sets the minimum width
 - `orientation = 90` rotates the document using a specified value : `-90` to turn left, `90` to turn right or `180` to flip the document
 - `isPaper = true` removes the background of the document's buttons (action and close buttons)
 
*Video :*
 - `video.loop = true` enables loop mode for the video player. 

[Back to the menu](index.md)
