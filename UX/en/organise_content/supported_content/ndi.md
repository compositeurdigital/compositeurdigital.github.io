# NDI

## Summary
* [Description](#description)
* [Content extension](#content-extension)
* [Discover available streams](#discover-available-streams)
* [Access a known stream](#access-a-known-stream)

## Description

Discover and play back NDI video streams form the local network.

> This functionnality is in beta stage and only avalaible in specific build of the application.

## Context extension

To automatically list all streams available on the network, create a folder with the `.ndi` extension.

To access a known stream, create a text file with the `.ndi` extension.


## Discover available streams

1. In your universe folder, create a folder named `<Name of your folder >.ndi` (e.g. `NDI streams.ndi`).

> When opening this discovery folder in the application, all available streams will be displayed with their respective identifiers in the form `<host name> (<stream name>)`. Take note of these identifiers to create direct access to each stream.

## Access a known stream

1. In your universe folder, create a text file named `<Name of your file>.ndi` (e.g. `Video stream.ndi`).
2. Open the file and add the following line to indicate the name of the NDI stream source : <br/>
`source = <host> (<stream name>)`

The `path` should be [relative](https://docs.microsoft.com/en-US/dotnet/standard/io/file-path-formats). 


[Back to Supported Content](index.md)

