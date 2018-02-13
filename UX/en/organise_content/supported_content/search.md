# Documentation

## Search

This content type allows you to display a search interface for any item (e.g. apartments, plans, cars, ect) that is placed in the same folder.

### Action within Compositeur Digital UX

- [X] Select filters to apply on the items, amongst a set of filters
- [X] Visualise search results on the same interface (e.g. using `.filter` extension) or on another page (e.g. using `.search` or `.apartments` extensions.
- [X] Open an item from the result page in the workspace.
- [X] Make a copy of the search interface using the `Duplicate` action.
- [X] Add the search interface to your favorite, using the `Add to favorites` action.
- [X] Remove the search interface from your favorites, using the `Remove from favorites` action.

### Content extension

To use a search interface, put all the items you need in a folder, and add the extension `.filter` or `.search` or `.apartments` (for real estate needs) at the end of the name of your folder.

Inside your folder, provide a file named `_list.csv`.

#### Spreadsheet : \_list.csv

This file contains the set of data which will be used for search criteria. This document is a `.csv` file, using `;` as delimiters. It can be edited using Microsoft Excel. 

**Format**

The first line of the spreadsheet represents the *type of criteria*. Select one amongst the following:
* *id* : **MANDATORY**. This columun must match with a document name in the folder. It will not be displayed as a criteria but will be used to open a result.
* *double* : criteria to display a decimal number.
* *float* : criteria to display a decimal number
* *int* : criteria to select an integer.
* *multiple* : criteria for multiple selection.
* *price* : represents a price. Do not specify unit.
* *single* : criteria for single choice
* *string* : criteria for multiple selection.
* *surface* : represents a surface. Type in "m²". Do not specify unit.
* *floor* : floor level (real estate use case)
* *orientation* : criteria to select an orientation (e.g. "North", "South"... real estate use case)
* *state* : criteria to select a state (real estate use case)
* *type* : number of room (real estate use case)
* *visual* : criteria to select a visual (real estate use case)

The second line of the spreadsheet represents the criteria name, which will be displayed in the search interface.

Starting from the third line, each line represent an item that can be searched using the search interface.

#### `.search` Extension

The `.search` extension is useful to display a search interface that is not dynamic. The user is selecting all the filters she wants to apply, and then press a button labelled "Search". The search results are computed and the items matching the criteria are displayed.

If the user presses the back arrow at the top left corner of the view, the filters can be changed.

The design of a result item corresponds to a thumbnail of the item, and its name.

#### `.filter` Extension

The `.filter` extension provides a dynamic search interface. Each time the user is changing a filter, the results displayed on the right side of the view are automatically updated to match the current selection.

The design of a result item corresponds to a thumbnail of the item, and its name.

#### `.apartments` Extension

The `.apartment` extension uses the same interface as the `.search` extension. The only difference is how the result looks.

The design of a result item indicates various information about the item : surface, orientation, type, floor, ect...

### Create a search interface

1. In your universe, create a folder named `<Name of your search interface>.search` or `<Name of your search interface>.filter` or `<Name of your search interface>.apartments` depending of the type of view you prefer (e.g. `Search.search`, or `Search.filter`).
1. Inside this folder, create a file called `_list.csv`. 
1. Fill the spreadsheet with the criteria you want, and describe your item.
1. For each item that belongs to the column `id` of your `_list.csv`, add an item inside your search folder (image, pdf, ect...)

Next : [Seqences : Pre-rendered 360° view (orbital, Compositeur Digital UX format)](sequences.md)

[Back to Supported Content](index.md)
