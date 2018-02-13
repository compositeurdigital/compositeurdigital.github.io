# Create a universe

Compositeur Digital UX processes documents stored on a specific location in your computer. Those documents can be organized in folders to facilitate the presentation.

## Required skills and resources

The preparation of a universe is done using the Microsoft Windows built-in file explorer application

You should be confortable with : 

- Organizing folders 
- Renaming files and folder
- That's all :relaxed:

## File extensions

Compositeur Digital UX uses the file extension to setup the various elements of a universe.  The `file extension` indicating the type of document is usually a set of 3 to 4 characters following the dot in the file name :

- Images : e.g. `photo1.jpg`, `photo2.png`.
- Presentation : e.g. `pres1.pptx`, `pres2.pdf`
- Text file : e.g. `table of content.txt`

By default the Windows File explorer application hides file extensions. We strongly recommend to change this setting.

## Universe

Technically, a universe is materialized as a folder on your computer. By default Compositeur Digital UX will look for content located in `Documents\Compositeur Digital UX`

To create your own universe, you can duplicate an exisiting one in the default location: `Documents\Compositeur Digital UX`.

## Background

You can customize your universe by changing the background image. To do so, simply add an image file (`.png` or `.jpg`) named `_background` in the universe's folder.

## Folders

You can organize your documents in folders and sub-folders. 

The first level of folders is displayed in Compositeur Digital UX in the dock located at the bottom of the universe view. 

>### <a name="contentFolder"></a> Hidden folders feature
>
>Folders using `.content` in their name will not be displayed in Compositeur Digital UX.
>See interactive slideshow to see the common use of this feature.

## Documents

Simply drag and drop your documents in the folders and sub-folders to populate your environment.

Check the Supported content for an exhaustive list of supported file types.

## Content viewing order

Compositeur Digital UX will display folders and documents in alphabetical order. You can however force a specific viewing sequence for documents and folders by prefixing the file name or folder name with a number. Compositeur Digital UX will not display the numbers but will arrange the items accordingly.

## Thumbnails 

The Compositeur Digital will automatically create thumbnails for all documents. You can customize the thumbnail of each document or folder of your universe.

### Folder thumbnail

If a thumbnail image has not been defined for a folder, the Compositeur Digital will auto-create a thumbnail image based on the first document of the folder.

To create a thumbnail for a folder simply drag and drop an image file named `_preview` (`.png` or `.jpg`) directly in the folder:

### Document thumbnail

To customize the thumbnail image of a document, drag and drop an image file using the same name but suffixed with `_preview` in the same folder.

Next : [Supported Content](supported_content/index.md)

[Back to Organise Content](index.md)
