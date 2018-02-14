# Sequences : 360° view

This content type allows you to display a 360° view of any objects, using a sequence of pre-rendered images (e.g. buildings).

![Sequence with several layers](../../img/content_sequence.JPG)

## Actions within Compositeur Digital UX

Sequences support the following action. To have a complete overview of each action, [see the section Actions](actions.md)

**Actions menu**

| Annotate | Capture  | Duplicate | Save as  | Selection | Share    |
|:--------:|:--------:|:---------:|:--------:|:---------:|:--------:|
| &#x2716; | &#x2714; | &#x2714;  | &#x2716; | &#x2714;  | &#x2716; |

**Interaction with the item**

| Layers   | Move     |
|:--------:|:--------:|
| &#x2714; | &#x2714; | 

## Content extension

To use a sequence, put all the images which are composing your sequence in a folder, and add the extension `.sequence` at the end of the name of your folder. Inside your sequence, only use files that end with `.jpeg`, `.jpg` or `.png`.

## Create a sequence

1. In your environment folder, create a folder named `<Name of your sequence>.sequence` (e.g. `My sequence.sequence`).
2. Drag and drop all the files which are composing your sequence in this folder.

## Layers

If you have multiple layers to display (the different floors of a building for example), you can organize your images folders for each layer, and put them in a global .sequence folder.

Here is an example :

* Building.sequence
  * Floor 1
    * 001.png
    * 002.png
...
  * Floor 2
    * 001.png
    * 002.png
...

Layers will be ordered by their names, from bottom to top, i.e. :

...
* Floor 2
* Floor 1

Next : [Mortgage Simulator (Compositeur Digital UX format)](simulator.md)

[Back to Supported Content](index.md)
