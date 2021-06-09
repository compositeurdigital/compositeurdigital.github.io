# Create your universes

Compositeur Digital UX processes documents stored on a specific location in your computer. Those documents can be organized in folders to facilitate the presentation.

## Summary
* [Required skills and resources](#required-skills-and-resources)
* [File extensions](#file-extensions)
* [Universe](#universe)
* [Background](#background)
* [Interactive background](#interactive-background)
* [Folders](#folders)
  * [Hidden folders feature](#hidden-folders-feature)
* [Documents](#documents)
* [Content Viewing Order](#content-viewing-order)
* [Thumbnails](#thumbnails)
  * [Folder thumbnail](#folder-thumbnail)
  * [Document thumbnail](#document-thumbnail)
* [Customize the workspace](#customize-the-workspace)
* [Demo Universe](#demo-universe) 


## Required skills and resources

The preparation of a universe is done using the Microsoft Windows built-in file explorer application

You should be confortable with : 

- Organizing folders 
- Renaming files and folder

## File extensions

Compositeur Digital UX uses the file extension to setup the various elements of a universe.  The `file extension` indicating the type of document is usually a set of 3 to 4 characters following the dot in the file name :

- Images : e.g. `photo1.jpg`, `photo2.png`.
- Presentation : e.g. `pres1.pptx`, `pres2.pdf`
- Text file : e.g. `table of content.txt`

By default the Windows File explorer application hides file extensions. We strongly recommend to change this setting.

![Turn on File Extensions](../img/enable_file_extensions.JPG)

## Universe

Technically, a universe is materialized as a folder on your computer. By default Compositeur Digital UX will look for content located in `Documents\Compositeur Digital UX`

![Universe folder](../img/universe_folder.JPG)

To create your own universe, you can duplicate an exisiting one in the default location: `Documents\Compositeur Digital UX`.

## Background

You can customize your universe by changing the background image. To do so, simply add an image file (`.png` or `.jpg`) named `_background` in the universe's folder.

![Universe background folder](../img/universe_background.JPG) ![Universe background Compositeur Digital UX](../img/universe_background_cdux.JPG)

### Handle ratio of your screen

Different backgrounds can be defined, adapted to different screen ratio. For example, a file named `_background3_2` will be selected if the app is running on a device which matches a 3:2 screen.

Here is a list of all supported screen format.

| Ratio | Background name    |
|:-----:|:------------------:|
| 3:2   | `_background3_2`   |
| 4:3   | `_background4_3`   |
| 5:4   | `_background5_4`   |
| 16:9  | `_background16_9`  |
| 16:10 | `_background16_10` |

Using different background files, adapted to different screen ratio allows you to make sure you can show your universe on any screen.

## Interactive Background

If you want to have an interactive background, which contains hyperlinks to display your content, it is also possible. Prepare a powerpoint file, with one slide containing your background image. In this slide, do not forget to create [Hot Spots](supported_content/powerpoint.md#hot-spots) to display your menus, or files. The name of the file should be `_background.pptx`. 

![Interactive background folder](../img/interactive_background.JPG)

## Folders

You can organize your documents in folders and sub-folders. 

The first level of folders is displayed in Compositeur Digital UX in the dock located at the bottom of the universe view. 

![Universe folder](../img/universe_background.JPG)
![Universe dock](../img/universe_dock.JPG)

>### Hidden folders feature
>
>Folders using `.content` in their name will not be displayed in Compositeur Digital UX.
>See [Powerpoints Hot Spots](supported_content/powerpoint.md#hot-spots) to see the common use of this feature.

## Documents

Simply drag and drop your documents in the folders and sub-folders to populate your universe.

Check the Supported content for an exhaustive list of supported file types.

## Content viewing order

Compositeur Digital UX will display folders and documents in alphabetical order. You can however force a specific viewing sequence for documents and folders by prefixing the file name or folder name with a number. Compositeur Digital UX will not display the numbers but will arrange the items accordingly.


## Thumbnails 

The Compositeur Digital will automatically create thumbnails for all documents. You can customize the thumbnail of each document or folder of your universe.

### Folder thumbnail

If a thumbnail image has not been defined for a folder, the Compositeur Digital will auto-create a thumbnail image based on the first document of the folder.

![No thumbnail](../img/universe_no_preview.JPG) 
![No thumbnail doc](../img/universe_no_preview_dock.JPG)

To create a thumbnail for a folder simply drag and drop an image file named `_preview` (`.png` or `.jpg`) directly in the folder:


![With thumbnail](../img/universe_preview.JPG) 
![With thumbnail doc](../img/universe_preview_dock.JPG)

### Document thumbnail

To customize the thumbnail image of a document, drag and drop an image file using the same name but suffixed with `_preview` in the same folder.

![With document thumbnail](../img/universe_document_preview.JPG) 
![With document thumbnail doc](../img/universe_document_preview_dock.JPG)

## Customize the workspace

It is possible to change the menu icon. By default, we use a "hamburger" menu icon. You can provide your own icon. Simply add a `.png` file named `_sidemenuicon.png` at the root of your universe.

You can also hide the three dots of the bottom bar when the bar is collapsed. Add a `_meta.txt` file with a line `hideBottomBarDots = true`.

![Customized workspace](../img/universe_custom_ui.JPG)

## Demo Universe

A Demo universe is available and can be [downloaded here](Demo-Universe.zip). Once downloaded, unzip the file and put the content inside your `Compositeur Digital UX` folder. This demo universe includes samples for each type of content you can create within Compositeur Digital UX.

Next : [Supported Content](supported_content/index.md)

[Back to Organise Content](index.md)
