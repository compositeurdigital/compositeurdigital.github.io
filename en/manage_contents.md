# Content management

The Compositeur Digital processes documents stored on a specific location in your computer. Those documents can to be organized in folders to facilitate the presentation

## Required skills and resources

The preparation of an environnement is done using the Microsoft Windows built-in file explorer application

You should be confortable with : 

- Organizing folders 
- Renaming files and folder
- That's all :)

### File extensions

The Compositeur Digital uses the file extension to setup the various elements of an environment.  The `file extension` indicating the type of document is usually a set of 3 to 4 characters following the dot in the file name :

- Images : photo1.jpg, photo2.png
- Presentation : pres1.pptx, pres2.pdf
- Text file : table of content.txt

By default the Windows File explorer application hides file extensions. We strongly recommend to change this setting:

![show extensions](img/show_extensions.jpg)

## Environment

The Compositeur Digital can be use for various use-cases

Real estate

![univers 1](img/univers1_v2.jpg)

Banking services

![univers 2](img/univers2_v2.jpg)

Technically, an environment is materialized as folder on your computer. By default the Compositeur Digital will look for content located in `Documents\Compositeur Digital`

![Environement view using the built-in Window file explorer](img/explorer_univers.jpg)

To create your own environment, you can duplicate an exisiting one in the default location: `Documents\Compositeur Digital`.

## Background

You can customize your environment by changing the background image. To do so, simply add an image file named `_background` in the environment's folder as described below:

![universe background](img/explorer_background.jpg)

## Folders

You can organize your documents in folders and sub-folders. 

The first level of folders is displayed in the Compositeur Digital in the dock located at the bottom of the environment view : 

![explorer root folders](img/explorer_root_folders.jpg)

![root folders](img/root_folders.jpg)

>### <a name="contentFolder"></a> Hidden folders feature
>
>Folders using '.content' in their name will not be displayed in the Compositeur Digital.
>See [interactive slideshow](slideshow#interactive) to see the common use of this feature.

## Documents

Simply drag and drop your documents in the folders and sub-folders to populate your environment.

Check the [Supported content](content_types.md) for an exhaustive list of supported file types.

## Content viewing order

The Compositeur Digital will display folders and documents in alphabetical order. You can however force a specific viewing sequence for documents and folders by prefixing the file name or folder name with a number. The Compositeur Digital will not display the numbers but will arrange the items accordingly.

>Note : If you ever need to display a file with a name starting with a number (e.g. `3D render`) please refer to the [Advanced configuration](config#configuration_dun_document) section.

## Thumbnails 

The Compositeur Digital will automatically create thumbnails for all documents. You can customize the thumbnail of each document or folder of your environment.

### Folder thumbnail

If a thumbnail image has not been defined for a folder, the Compositeur Digital will auto-create a thumbnail image based on the first document of the folder:

![explorer no preview folder](img/explorer_nopreview_folder.jpg)

![no preview folder](img/nopreview_folder.jpg) 

To create a thumbnail for a folder simply drag and drop an image file named `_preview` (.png or .jpg) directly in the folder:

![explorer no preview folder](img/explorer_preview_folder.jpg)

![no preview folder](img/preview_folder.jpg) 

### Document thumbnail

To customize the thumbnail image of a document, drag and drop an image file using the same name but suffixed with `_preview` in the same folder:

![explorer preview file](img/explorer_preview_file.jpg)

## Stand by video

When the Kiosk mode is activated a fullscreen video can be automatically started after a specified period of inactivity. The video will loop until the touch screen is activated.

Place a supported video file named `_standby` in the environment's folder:

![standby](img/explorer_standby.jpg) 

Check the [supported video types](video.md) section for further details.
