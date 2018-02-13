# Documentation

## Panorama : 360° view

This content type allows you to display a 360° view of a scene (e.g. landscapes, interior views...) using specific images.

### Action within Compositeur Digital UX

- [X] Enable / Disable navigation mode.
- [X] In navigation mode, sliding your finder on the item rotates the camera inside the scene.
- [X] Make a copy of your panorama using the `Duplicate` action.
- [X] Make a capture (i.e. create an image of the current view) using the `Capture` action.
- [X] Add the panorama to your favorites, using the `Add to favorites` action.
- [X] Remove the panorama from your favorites, using the `Remove from favorites` action.

### Content extension

To use a panorama, put the images to render in a folder, and add the extension `.panorama` at the end of the name of your folder.
Inside your panorama, only use files that end with `.jpeg`, `.jpg`, `.png`.

### Create a panorama

1. In your universe folder, create a folder named `<Name of your panorama>.panorama` (e.g. `My Panorama.panorama`).
2. Drag and drop all the files which are composing your panorama in this folder.

### Projection types

Two types of projection are supported.

#### Spherical projection

Place a single image with the spherical projection of the scene in the folder. 

**Important** : Do not place any other images in this folder (except `_preview` files).

#### Cube projection

Place 6 images, corresponding to the six faces of your cube in the folder.

**Naming** : your files should respect the following conventions:
   * *up* : named "u" or matches "\_u\_", "\_u", "u\_", "up" (e.g. "u.jpg", "pano_u.jpg", "up.jpg")
   * *down* : named "d" or matches "\_d\_", "\_d", "d\_", "down" (e.g. "d.jpg", "pano_d.jpg", "down.jpg")
   * *front* : named "f" or matches "\_f\_", "\_f", "f\_", "front" (e.g. "f.jpg", "pano_f.jpg", "front.jpg")
   * *back* : named "b" or matches "\_b\_", "\_b", "b\_", "back" (e.g. "b.jpg", "pano_b.jpg", "back.jpg")
   * *left* : named "l" or matches "\_l\_", "\_l", "l\_", "left" (e.g. "l.jpg", "pano_left.jpg", "left.jpg")
   * *right* : named "r" or matches "\_r\_", "\_r", "r\_", "right" (e.g. "r.jpg", "pano_r.jpg", "right.jpg")

**Important** : Do not place any other images in this folder (except `_preview` files).

Next : [Quizz (Compositeur Digital UX format)](quiz.md)

[Back to Supported Content](index.md)

