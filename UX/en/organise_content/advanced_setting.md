# Advanced settings : metadata

You can modify a document's behavior or associated actions using specific parameters described in a file named `_meta.txt`.

To modify the behavior of a folder in the application, the meta file must be placed inside the targeted folder, and named `_meta.txt`.

To modify the behavior of a document in the application, the meta file must be named after the document's file name followed by the suffix `_meta` and the `txt` extension. It must be saved at the same location as the target document. 

> Example: for a file named `1 - image.jpg`, the corresponding meta file should to be named as follows : `1 - image_meta.txt`.

In the meta file, each line (called `meta`) shall describe a parameter using the following structure: `metaName = value`

A binary meta (true or false) is described as follows:  `metaName = true`. It's default value is `false`. The values `1` (true) and `0` (false) can also be used.

To apply a specific behavior to a set of documents, use the `*.` prefix on the description of the meta and save the meta file in the folder containing the set of targeted documents

> Example : `*.table.hideCommands = true`


## Metadata supported

| Metadata Key                      | Value            | Description                                                                 |
|:---------------------------------:|:----------------:|:----------------------------------------------------------------------------|
| `desiredHeight`                   | 400 (number      | sets the default height of the document                                     |
| `desiredWidth`                    | 400 (number)     | sets the default width of the document                                      |
| `isPaper`                         | true/false - 1/0 | removes the background of the document's buttons (action and close buttons) |
| `maxHeight`                       | 400 (number)     | sets the maximum height                                                     |
| `maxWidth`                        | 400 (number)     | sets the maximum width                                                      |
| `minHeight`                       | 400 (number)     | sets the minimum height                                                     |
| `minWidth`                        | 400 (number)     | sets the minimum width                                                      |
| `orientation`                     | 90 (number)      | rotates the document using a specified value : `-90` to turn left, `90` to turn right or `180` to flip the document |
| `simulator.creditMaxValue`        | 800000 (number)  | sets the maximum value of a loan                                            |
| `simulator.creditTickFrequency`   | 5000(number)     | sets the interval between two values for a loan                             |
| `simulator.creditDefaultValue`    | 3000000 (number) | sets the default loan value                                                 |
| `simulator.durationMinValue`      |   5 (number)     | sets the shortest duration of a loan                                        |
| `simulator.durationMaxValue`      |  30 (number)     | sets the longest duration of a loan                                         |
| `simulator.durationTickFrequency` | 1 (number)       | sets the interval between two values for a loan duration                    |
| `simulator.durationDefaultValue`  | 20 (number)      | sets the default duration of a loan                                         |
| `table.hideCommands`              | true/false - 1/0 | hides the control buttons of a document. On a slideshow, the buttons `<` and `>` will disappear. |
| `table.noRotate`                  | "                | inhibits rotation for the document                                          |
| `video.loop`                      | "                | enables loop mode for the video player                                      | 

<!--| `table.noScale` | " | inhibits resizing for the document |-->
<!--| `table.noMove` | " | inhibits moving the document | -->

[Back to Organise Content](index.md)
