# Shortcuts, hyperlinks : CDURL

## Summary
* [Description](#description)
* [Actions within Compositeur Digital UX](#actions-within-compositeur-digital-ux)
* [Content extension](#content-extension)
* [Create a guestbook](#create-a-guestbook)
* [Download a sample](#download-a-sample)

## Description

This content allows you to create links to documents inside your universes. Imagine you have an image or a document that you would like to see in two differents folders. Using a `cdurl` file, you can create an hyperlink to the file which will be inside a different folder.

Using `.cdurl` allows you to handle the amount of memory and disk space consumed by your universe. 

## Context extension

To create a shortcut to a document, add the extension `.cdurl` at the end of a text file.

## Create a cdurl

1. In your universe folder, create a file named `<Name of your file>.cdurl` (e.g. `File shortcut.cdurl`).
1. Open the file and add the following line to indicate the path to the existing file : <br/>
`url = <relative path to the document>`

The `path` should be [relative](https://docs.microsoft.com/en-US/dotnet/standard/io/file-path-formats).  

## Download a sample

A Demo Universe which contains a sample for the guestbook is available, [give it a try!](../Demo-Universe.zip) &#x1f604;

Next : [Panorama : 360° view (first person, Compositeur Digital UX format)](panorama.md)

[Back to Supported Content](index.md)

