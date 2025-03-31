# Release notes

### 4.3.6563 - March 31, 2025

- PDF rendering with PDFium available for installes from Windows Store

### 4.3.6520 - March 19, 2025

- [FIX] Rendering issue for some PDF files

### 4.3.6278 - January 31, 2025

- [FIX] Preconfigured save folder is not applied

### 4.3.6235 - January 27, 2025

- [FIX] Interactive areas become inactive after the document has been pinned or taped
- [FIX] Some folders synchronized with OneDrive are incorrectly marked read-only


### 4.3.6159 - January 14, 2025

- Reverted function of stylus barrel button to eraser from dynamic ink

### 4.3.6154 - January 13, 2025

- [FIX] Slideshow internal navigation and universe selector links

### 4.3.6129 - January 10, 2025

- [FIX] Approximative/incorrect ink to text recognition
- [FIX] Documents added by drag and drop are stuck if the origin templage group is closed
- [FIX] Random crash when opening a file upload activity from the "Get a transfer link" action
- [FIX] The "Get a transfer link" action does not function when selected from the imported document list
- [FIX] Miracast error when quickly opening/closing or refreshing a project repeatedly
- [FIX] Error when My OneDrive is not available during tutorial
- [FIX] Error loading .cdux project files
- [FIX] Attempts at fixing elusive crash on document opening
- [FIX] Missing warning message When unpluging the removable storage that contains the current universe

### 4.3.6080 - January 6, 2025

- [FIX] Some older Outlook mail boxes aure not detected
- [FIX] Occasional crash when opening documents
- [FIX] Tape visual is not resized to match document size

### 4.3.6013 - Decembre 18, 2024

- MXF video format support (Studio edition)
- Support for RTP, RTSP, HTTP video streams (Studio edition) 
- Video: optional quick rewind of a few seconds with `video.fastrewind.duration`
- Dynamic ink: draw annotations that show for a few seconds on playing videos or any documents
- Warn if pre-configured universe location is not available
- Folders named "Compositeur" "Excense", "CDUX" are recognized as universe sources
- [FIX] Designer and project saving not available for "This computer > Documents" when Onedrive documents backup is enabled
- [FIX] Annotations can be drawn outside some non-rectangular stickers
- [FIX] Some activations errors are not explicit, eg. proxy auth errors

### 4.2.5974 - December 10, 2024

- Support for migration from 3.x installs with automatic login
- [FIX] Error when closing a project immediately after having opened it
- [FIX] Universes contextual menus are available in kiosk mode
- [FIX] Error when refreshing a universe when OneDrive synchronizes personal documents

### 4.2.5944 - November 22, 2024

#### New features

- New color palette and new control pane for annotations without digital pen
- Add notes, blank sheets and other templates by drag and drop from the side menus
- Drag and drop files from File Explorer to import them
- Web pages can be resized
- New document import method: quick transfer from collaborative activities
- Notes and blank sheets: dictation to add text (Windows 11 only)

#### General improvements and fixes

- Notes added via the new note button appear at the same size as their note of origin
- Documents stay visible after being detached from the document they were taped on
- More progressive stroke thickness variation based on pressure from stylus that support pressure
- Application version available from side me settings panel
- Mouse annotations can now be activated by pressing `D` to draw, `E` to erase
- New parameters do disable document manipulation inertia: meta `table.noInertia=true`, setting `cdux.workspace.manipulation.disableInertia=true`
- Web memory: new HTML message styling for share methods other than an email message
- Retain web pages actual uri to restore their state
- Reduced minimal capture area
- [FIX] Conversion of PowerPoint files from a Teams library generates a bitmap pdf even when a vector render is possible 
- [FIX] Collaboratives activities failure after stopping an activity then starting another 
- [FIX] Recently created Teams channels are not visible from the add source dialog 
- [FIX] Capture and import fail when working offline in a universe from a OneDrive source 
- [FIX] Projects created in a OneDrive source appear twice in the project list
- [FIX] Interactive HTML view no longer respond to touch taps after having been moved
- [FIX] Collaboratives activities: chaining remote presentations cause an error
- [FIX] Some vote results stickers cannot be resized
- [FIX] Annotation strokes added via remote presentations are randomly deleted
- [FIX] Captures sent to web memory include black rounded corners
- [FIX] Tape indicators are not visible when energy saving mode is active
- [FIX] Low performance on SurfaceHub 2S, new global parameter `disableEffects`
- [FIX] Error when cancelling upload of a web memory
- [FIX] Random error when closing a search module 
- [FIX] Notes and blankshet sometimes lock out of text input with a virtual keyboard
- [FIX] Virtual keyboard is not shown for web views
- [FIX] Designer: error when renaming an custom interactive web view
- [FIX] Designer: error when opening an custom interactive web background
- [FIX] Designer: unexpected reset of maps display style
- [FIX] Crash when loading projects in Teams/SharePoint sources containing a very large number of projects
- [FIX] Designer tab unavailable if This computer > Documents does not contain a folder named Compositeur Digital UX
- [FIX] Designer: interactive web view cannot handle items with a `#` in their file name
- [FIX] Double-clicking the save button may cause an error followed by a later crash 
- [FIX] "Created by" is lost when saving a project
- [FIX] Sequence view slider is shown behind menu button
- [FIX] Cannont move search results with map results
- [FIX] Tab selector is visible in kiosk mode


### 4.1.5865 - October 31, 2024

- [FIX] Full size captures are created twice in some cases

### 4.1.5639 - September 5, 2024

- [FIX] Webview: inaccessible scrollbars
- [FIX] Webview: cannont select text in text inputs
- [FIX] Calculator buttons are misaligned
- [FIX] Designer: treeview contextual menu does not match selection on Windows 10

### 4.1.5526 - July 11, 2024

- [FIX] Attached files missing when sharing with Outlook

### 4.1.5507 - July 8, 2024

- [FIX] App fails to launch for new installs from 'online install' link

### 4.1.5501 - July 5, 2024

#### New features

- New share experience unifying web memory and file sharing
- New capture tool: capture a selection or the whole document view
- Outlook client share target automatically enable if found install from Office 15 or 16
- New web page import experience
- Designer: New interface for web link creation
- New network share connector, synchronizes documents like Teams/SharePoint

#### General improvements and fixes

- Use web page icons as preview
- Share with Outlook MS365 only available if the user is currently connected
- Option to display a button to hide the bottom bar: `bottombar.showQuickHideAction=true`
- Zoom with mouse wheel is reduced
- Designer: support for additionnal templates from a network share
- Designer: disable actions to add, delete, move, rename documents with meta parameters `editor.disableAdd`,  `editor.disableMove`, `editor.disableRename`, `editor.disableDelete`
- Designer: template elements can be made invisible
- [FIX] Undesired click triggered after html view is moved
- [FIX] Unreadable mp3 file icon
- [FIX] Project export fails
- [FIX] Crash using keyboard shortcutes in certain conditions
- [FIX] Univers designer is not the exact aspect ratio selected
- [FIX] Dynamic HTML designer crash
- [FIX] Miracast display does not start
- [FIX] Changed Miracast receiver name to 'CDUX  machine' for a better identification
- [FIX] Nearby sharing not completing
- [FIX] Incomplete template creation in designer after renaming or moving an element
- [FIX] Designer zoom
- [FIX] Designer for dynamic HTML does not always follow selection
- [FIX] Panorama/3D objects: crashes can occur when the manipulation action no longer reflect the actual state
- [FIX] Crash on closing or bringing elements to the front


### 4.0.5387 - May 27, 2024

- [FIX] Advanced configuration or the start page layout

### 4.0.5297 - April 15, 2024

[FIX] Text entered in PowerPoint templates missing in exported PDF if document was closed when sharing

### 4.0.5263 - April 2, 2024

[FIX] Cannot import some web links for clipboard
[FIX] Access error when editing MS365 documents online

### 4.0.5207 - March 14, 2024

- [FIX] Missing catalog search results after case change

### 4.0.5193 - March 5, 2024

- Support for mutliple slide PowerPoint universe selectors
- Video: Play/Pause action is always visible, unless explicitely disabled with `actions.playpause.disabled=1`
- [FIX] Error when automatic universe reset occurs in Kiosk mode
- [FIX] Invalid actiovation state for some multi-user installs, if shared application data is enabled
- [FIX] PowerPoint universe selectors not updated if changed
- [FIX] Univers designe pannel cannot be disabled
- [FIX] Activities: sketch vote results visuals do not match the actual drawings 
- [FIX] Designer: universe properties, including background selection, are not displayed
- [FIX] Unwanted closing of documents on tap for some large touch screen devices
- [FIX] Installation script closes its terminal on success


### 4.0.5082 - February 14, 2024

#### New features

- New integration of PowerPoint presentations, with improved render for some graphs and fonts
- New visual design for the documents menu and actions
- Search function available from the documents menu
- New visual design for the integrated universe designer
- New interaction mode for web pages:
    - Clicking, tapping and typing are available directly without switching mode 
    - While in touch interaction mode, pages can be moved and resized from their border
- New online activities, with a renewed visual design:
    - Multiple vote formats (Yes/No, True/False, ❤️/💔, rate 1 to 5)
    - Vote for a sketch
    - Broadcast documents to all participants
- Web memory: dashboard of shared souvenirs from the home page as an option


#### General improvements and fixes

- Support for hyperlinks in imported PDF/PowerPoint files
- Activities: new link/QRCode style with copy and share actions
- Activities: link/QRCode displayed when starting a session
- MS365 Outlook: select a current or recent meeting as subject for the e-mail
- Web memory: new style for the link to share
- Web memory: assign the actual recipients from sent email when sent with Outlook
- Notes and blank sheet: web link detection from typed or pasted text
- Move animation when `desiredposition` is specified
- Rounded corner in proportion with the document size with parameter `cornerRadius` 
- [FIX] Thumbnails not displayed on first display of a Teams/SharePoint universe
- [FIX] Currently displayed sub folders are not restored when loading a saved project
- [FIX] Web memory: e-mail composition does not allow entering more than two recipients
- [FIX] Catalog: lower and higher bounds cannot be reset from price filters
- [FIX] Designer: folders on network share cannot be removed
- [FIX] Designer: some integrated web app elements cannot be scrolled

### 3.7.4525 - October 10, 2023

- [FIX] Some PDF documents can become invalid after being shared

### 3.7.4373 - September 19, 2023

- [FIX] Share with Outlook stuck on white page

### 3.7.4149 - June 13, 2023

- Universe and imported documents' annotations and notes are preserved when saving projects
- [FIX] Crash on some devices with 175% dpi scaling
- [FIX] Document and universe previews not aligned
- [FIX] Documents are blurry during the appear animation
- [FIX] Share with MS 365 Outlook email attachments


### 3.7.3987 - April 13, 2023

- [FIX] Error when sharing web memory when current language is French
- [FIX] Outlook MS365 compose window not responding
- [FIX] PDF internal page orientation is lost on export if document has annotations
- [FIX] File transfer activity rejects all file types
- [FIX] Video background color not applied


### 3.7.3879 - March 24, 2023

- [FIX] Document menu still visible with parameter `nochromebuttons=true`


### 3.7.3800 - March 13, 2023

- [FIX] Application and camera capture inactive in import menu
- [FIX] Newly added documents missing when refreshing universe


### 3.7.3779 - March 7, 2023

#### New features

- Improved application statup time and universe loading time
- Webview2 as default if runtime if a suitable runtime is found
- Webview: new api call `getSessionSettings()` to get the current presenter side
- Share with Microsoft 365 Outlook: mail compose page integrated to the share experience
- Share with Microsoft 365 Outlook available for sharing a web memory link
- Share with Outlook app available when installed from Windows Store
- Activities: New serverless service excen.se
- Activities: New vote activity 
- Universe selector: interactive PowerPoint for universe selection 
- Universe designer: Select documents preview from an inline menu, with image paste support
- Universe designer: Common settings editable
- Universe designer: Powerpoint/PDF: interactive areas visualization
- Universe designer: Videos: playbakc settings (loop, mute, controls behavior)
- Universe designer: Navigation bar with current selection path and previous/next/parent actions 
- Universe designer: Drag and drop documents from file explorer
- Universe designer: Zoom on selected document

#### General improvements and fixes

- Web memory: Handle large volume of shared documents  
- New presenter side interface
- Powerpoint/PDF: improved loading and display time
- Product sheets: New style to match folder view
- Support for .csv data files that are not UTF8 encoded
- Support for Samsung Flip version 4 devices
- [FIX] PDF: Error displayed for absolute links
- [FIX] Manipulation locked on some devices with stylus support
- [FIX] Videos: play /pause button still visible despite `video.controls.hide=true` setting
- [FIX] Web memory: shared documents counted twice
- [FIX] Menu `open` action generates a PDF for images instead of opening the actual image
- [FIX] Sustom start page interface not applied when switching source
- [FIX] Webview: locked manipulations
- [FIX] External projects do not load if their name includes special characters
- [FIX] Crash after a short time for some univers containing panoramas
- [FIX] Panoramas: the rendering of preview can hang all future renders
- [FIX] Catalog: error when text input stays open
- [FIX] Catalog: manipulation not recognised if started from results list 
- [FIX] Background videos not played in a loop
- [FIX] Document menu: cropped selection indicator


### 3.6.3619 - February 2, 2023

- [FIX] Excessive memory consumption for universes with many PowerPoint documents

### 3.6.3226 - October 5, 2022

#### New features 

- Updated UI to match Windows 11 visual style with rounded corners and folders redesign
- TV Studio mode and other feature packs
- Import video streams from webcams and video capture devices
- Web memory: option to generate a shareable link rather than having the platform sending an email
- Miracast display host support (on Windows 11)
- Webview2 rolling out

#### General improvements and fixes
 
- New `noHistory=true` parameter to prevent documents from appearing in the recycle bin
- Surface pen button support: press to advance to the next slide, long press to return to previous 
- Powerpoint backgrounds now export in Web memory & Companion apps
- Slideshow: Create multiple version of a document with parameter `?newInstance=true` in hypertext links
- Webview: new apis  ([see documentation](../organise_content/supported_content/web_page.html)))
- Videos: Timestamp & playlist hints

- [FIX] Web memory: display aspect ratio lost on 
- [FIX] Video thumbnails missing in some cases
- [FIX] sticked/taped documents restored at the wrong size when opening a project- [FIX] Video loop state lost after project reload
- [FIX] Fallback to closest aspect ratio background when no exact match
- [FIX] Source settings not applied when swithcing sources
- [FIX] empty universe projects thumbnail show trasparent background
- [FIX] Escape key does not gracefully exit the Share dialog
- [FIX] Menu appears at the top left after unpin
- [FIX] exception when loading video thumbnail in history
- [FIX] Activities appear centered, as opposed to templates/notes that appear on the side
- [FIX] File upload activity 'file type not supported' error


### 3.5.3069 - August 31, 2022

- [FIX] Webview2: crash when leaving a project with an HTML background

### 3.5.3047 - August 11, 2022

- New `hideBottomBar` parameter to completely hide the bottom bar when collapsed
- [FIX] PowerBI: reports not displaying

### 3.5.3016 - August 8, 2022

- WebView: `CDUX.FindItems()` now returns the item's preview & icon relative paths
- WebView: added `CUDX.ClearWorkspace()`

### 3.5.2994 - August 5, 2022

- [FIX] BoardItem crashes

### 3.5.2965 - July 25, 2022

- [FIX] Account settings not read when launching the app.

### 3.5.2928 - July 5, 2022

- Webview2: link to donwload and install the Microsoft Webview2 Runtime if missing
- [FIX] Standby video playback stops instead of looping back
- [FIX] SharePoint: documents not updated when refreshed

### 3.3.2871 - June 17, 2022

- [FIX] `themeColor` universe meta not applied

### 3.3.2856 - June 10, 2022

- New `desiredPosition` parameter ([see documentation](../organise_content/advanced_setting.html#metadata-supported)))
- [FIX] Video: play/pause still visible whe disabled with `video.controls.hide=true`
- [FIX] Powerpoint: render issues
- [FIX] SharePoint: documents not updated when refreshed
- [FIX] PowerPoint links to documents outside the current universe trigger an import

### 3.3.2813 - May 16, 2022

- Video: add .video folder extension to play a list of videos in sequence
- Video: rework video controls. Play/Pause action will always be available at the bottom right corner of the video. Full control can be shown on tap.
- 3D objects: handle shadows and ground textures.
- 3D objects: rework object orientation (.obj) for better positionning
- Product sheet: add `disableExport` to prevent an area from being exported
- PowerPoint: improved rendering of images
- Start Page: handles Category names and previews
- Slideshow: PowerPoint ratio extension is not ignored when the file is defined as the background.
- [FIX] Web view crashes when used a background.
- [FIX] Importing a URL won't load the web page

### 3.2.2769 - May 5, 2022
	
- Support for migrating locally saved projects when universe location is changed

### 3.2.2622 - March 21, 2022
	
- PowerPoint: improved rendering of cropped images	
- Product sheet: associated documents are now shared in addition to the pdf summary
- Catalogue: numeric filter with option to set a single minumum or maximum value
- Catalogue: placeholder for text filters
- Catalogue: selection summary for groupe and combined filters
- PDF/PowerPoint: orientation adjustments persist per user 
- SharePoint: stability and speed improvements
- Simplified experience to sart a remote document presentation activity
- PDF export for local web pages
- [FIX] Dynamics CRM: cannot share selection

### 3.2.2469 - February 21, 2022

- Catalog: direct input for minimum and maximum for numeric filters
- Catalog: sort by "Yes/No", "Oui/Non", ... values
- Support for license-activated features and feature packs
- Web memory: web pages exportable as a pdf with a preview and a link
- [FIX] PDF and PowerPoint pages loading sometimes hang when reloading an univers
- [FIX] Stickers shared if not sticked to a document
- [FIX] Stickers displayed as a black shape in the templates tool panel
- [FIX] Indexed panorama can not load
- [FIX] Sequences: interactive polygons not displayed
- [FIX] Stickers: setting a relative size (eg `desiredWidth=5%`) prevents `isSticker=true` behavior 
- [FIX] PowerPoint: deeplinks are not recognized if the document is part of an MS365 repository
- [FIX] Catalog: trimmed text on some numeric filters
- [FIX] OneDrive/SharePoint with USB cahce: missing metadata after second session in the same univers 
- [FIX] Slideshow: interactive elements do not follow rotation


### 3.2.2371 - December 28, 2021

- [FIX] Repeated user information access autorization prompt on shared devices
- [FIX] Catalog: crash when using special `round` result display

### 3.2.2307 - December 6, 2021

#### New features
- Web memory: store a view of your session in the cloud and share a personalized link to a web page containing your documents and notes

- Catalog: new cleaner search filters experience
- Catalog with map: direct touch manipulation of the map

#### General improvements and fixes
- Slideshow & images: new action to change a document orientation
- Slideshow: control where the previous/next button are shown with `slideshow.controls.position` ([see documentation](../organise_content/advanced_setting.html#slideshow))
- Stickers: define extra-small stickers with the parameter `desiredWidth`, suggested value `desiredWidth=40`
- Web: display the manipulation invite in the bottom right corner (instead of centerd ofer the page content) with `action.manipulation.location`
- Sharepoint & OneDrive: new connectors with differential updates for faster synchronization
- Settings: detailed application information
- General performance improvements
- [FIX] Toolbox: custom toolbox element are not available if standard templates are disabled
- [FIX] Panorama: spherical panoramas displayed with the wrong orientation
- [FIX] PowerPoint: links in SmartArt elements not recognized
- [FIX] Cannot open files with Compositeur Digital UX from file explorer
- [FIX] Timers: the progress ring does not indicate the remaining/elapsed time


### 3.1.2172 - November 16, 2021 

- [FIX] Kiosk: does not reset to the default univers after standby expiration

### 3.1.1970 - September 16, 2021 

- [FIX] Webview: captures are not made at the correct resolution

### 3.1.1956 - September 15, 2021 

- New UI matching Windows 11 visual style
- [New share experience](../img/share.jpg)
- Performance improvements of universe loading
- Annotations: set the default inking color and size for an universe ([see documentation](../organise_content/advanced_setting.html#inking))
- Better positionning of documents with `desiredWidth` or `desiredHeight` values of 100% or over
- Catalog: large sets of options can be set to open in a popup to save space
- Catalog: added quarter range filter for dates
- Productsheet: popup for additionnal information
- Video: `video.backgroundColor` metadata to control the color shown while the video loads
- New `hideLinkTypeIcon` metadata to control the appearance of documents in a folder
- [FIX] Imported documents missing when saving a new project but not closing it
- [FIX] 'Rename project' actually creates a copy
- [FIX] PowerPoint links with `#Page Name` anchors not recognized
- [FIX] SharePoint/OneDrive cache constantly growing
- [FIX] Activities service connection issues
- [FIX] Folders should not allow to navigate up to the productsheet they reside in
- [FIX] Crash on devices without removeble storage capabilitiy
- [FIX] Small stickers erratic behavior when moved


### 3.0.1737 - June 3, 2021 

- Search/Filter: `bannerColor` for first-level results
- Forms: `visiblewhen` conditions applicable to sub-form labels and the clearing of sub-form values is optional with `clearValues`
- Text inputs now selectable with mouse for easier editing and copying
- [FIX] Absolute links (such as generated by PowerPoint+SharePoint) not resolved if they contain accented characters
- [FIX] Combobox scaling issue in CRM connector 
- [FIX] Slideshow pages rendered multiple times on export if they contain text input
- [FIX] Saving a project with the same name as an existing one causes overwrite when using local storage policy


### 3.0.1689 - May 12, 2021 

- The order of selected documents is conserved between sessions
- [FIX] Documents still marked as selected after being taped or pinned
- [FIX] Application cannot be closed
- [FIX] Duplicated sync error icon
- [FIX] History not rememberd on resume after error
- [FIX] SharePoint/OneDrive: file modifications not detected in some cases
- [FIX] License account not shown on some versions of Windows 10


### 3.0.1606 - April 16, 2021 

- [FIX] Combobox scaling issue in forms 
- [FIX] Settings not applied when restoring a project


### 3.0.1586 - April 2, 2021 

- The rename project dialog includes the current name for ease of use
- [FIX] Cannot activate touch annotations from side menu
- [FIX] Theme not correctly reset when leaving a project


### 3.0.1572 - March 22, 2021 

- Annotations: quick mouse annotation by holding the *Ctrl* key or with the mouse's middle button
- Web: 'integrated' interaction mode support for number inputs
- Web: 'integrated' interaction mode shows the virtual touch keyboard for text or number inputs
- Rename projects from the project list or from the workspace
- Improved readability of source loading errors
- Ability to open a toolbox category by default with the [`toolbox.startOpened`](../organise_content/advanced_setting.html#metadata-supported) meta
- [FIX] Sequence pois inaccessible if displayed close to the bottom slider
- [FIX] Incorrect form layout when elements visibility change
- [FIX] Slideshow not always correctly updated from cloud-stored documents modifications
- [FIX] Combobox scaling issue in filters 
- [FIX] PDF and Powepoint links issues with empty links and web urls ending in  '/'
- [FIX] Powerpoint rendering issues
- [FIX] USB cache errors


### 3.0.1467 - February 5, 2021 
- [FIX] Importing multiple files at once could result in errors when saving a project

### 3.0.1457 - February 1, 2021
- Web links in PDF and PowerPoint presentation now open in a web view instead of the browser
- Added a default preview for empty product sheets
- Support for hostpot text color
- [FIX] Form combobox does not retain their value
- [FIX] Inconsistant UI between file transfer and notes activities
- [FIX] PowerPoint rendering issues
- [FIX] PDF and PowerPoint not refreshed when changed in SharePoint if using MS365 connector
- [FIX] Note activity assigned colors


### 3.0.1428 - January 12, 2021

#### New features
- Companion
- Web pages exportable as standalone html file
- Forms: [sub-form links](../organise_content/supported_content/form.html#form-links) and compact UI

#### General improvements and fixes
- [FIX] Powerpoint rendering issues
- [FIX] Annotations not saved in some cases
- [FIX] First attached note always restored at default size
- [FIX] Panorama loading error when encountering empty hotspots

### 2.2 - November 12, 2020
- Redesigned palette menu
- Save & exit action replaced with distinct Home and Save actions
- Quick empty workspace loading
- Code activation: device Id displayed in settings
- New Sharepoint connector with background synchronization
- Webp & jfif image format support
- Enhanced multi-touch manipulation pivot
- Scale ruler (preview)
- Webview new window setting in meta file
- New background
- [FIX] blurry image on mouse zoom
- [FIX] Lot of bug fixes

### 2.1.29 - May 4, 2020
- French translation for "Install demo contents" on shared  device.
- Maximise folder
- Catalog loading speed improved
- Project info in sidebar
- [FIX] AccessDenied Exception when importing files using OneDrive app on Surface Hub
- [FIX] Review prompt may cause errors
- [FIX] Store purchases not recognized
- [FIX] Error when entering partially-cached universe after updates were made on SharePoint/Teams

### 2.1.26 - March 11, 2020
- Webview 'Home' action allows to navigate back for pages without internal navigation
- Default menu actions can be displayed as shortcuts for one-click capture, selection, share, etc… See [Advanced settings](../organise_content/advanced_setting.html#menu-actions)
- [FIX] Crash when resuming video playback right after drawing annotations
- [FIX] Possible errors when first entering some very large Teams/Sharepoint universes

### 2.1.25 - March 6, 2020
- Support for ARM devices
- `table.alwayBehind`/`table.alwaysOnTop` metas to force documents to stay behind/over all other opened documents
- Search and filter projects, with new author info
- Annotation on web views
- Annotation on videos (when paused)
- Sidebar automatically pinned when in touch drawing mode
- Timer brought to the front when its alarm goes off
- Support for Samsung Flip 2 pen interaction
- Source-defined background applied in universes and during workspace loading
- Start page performance improvements
- Sidebar and main menu UI tweaks
- [FIX] Webview action buttons may be invisible on white pages
- [FIX] Forms with dynamic content may crash on some devices
- [FIX] CRM search: entity data not imported
- [FIX] Performance issue when displaying many notes
- [FIX] Template elements misalignment on some devices
- [FIX] Importing documents in a SharePoint/Teams project fail in some cases
- [FIX] Standby video cannot be stopped in some cases 
- [FIX] Error when cancelling Office 365
- [FIX] Error when using SharePoint/Teams sources with the cache on USB

### 2.1.20 - January 3, 2020
- Panorama: hotspots with icon and description or item link
- Common metadata to disable individual menu actions or all at once, see [Advanced settings](../organise_content/advanced_setting.html#metadata-supported)
- [FIX] PowerPoint rendering errors
- [FIX] Catalog: text filters cannot be applied to 1st level items

### 2.1.18 - December 5, 2019
- [FIX] Delay when entering an universe on Sharepoint/Teams
- [FIX] Office 365 account still displayed after signing out

### 2.1.16 - December 2, 2019
- Improved file operations
- Disabled the 'Refresh universe' action on empty universes
- [FIX] Application theme does not always follow the current background
- [FIX] PowerBI and Dynamics CRM authentication failure
- [FIX] Wrong indication when adding a Sharepoint library

### 2.1.15 - November 20, 2019
- [FIX] Incomplete universes when installing sample content

### 2.1.14 - November 18, 2019
- [FIX] Catalog: region filter always disabled

### 2.1.13 - November 8, 2019
- [FIX] Unable to save projects on Teams or Sharepoint libraries in some conditions

### 2.1.12 - November 4, 2019
#### New features
- Improved Sharepoint and Teams synchronization for faster loading of universes
- Customizable start page background
- Prompt for the recipient when sending a mail with SMTP or SendGrid
- Share the selection from the bottom bar
- Import from camera
- Timer with stopwach and countdown
- Pinnable side menus
- Share source from the start page list
- Loan simulator with "in fine" loan
- Support for trial codes

#### General improvements and fixes
- No slides overview for single-slide presentations
- Default previews for web and calculator
- New `Tools` templates category with timers and calculator
- Prevent closing of documents with the `table.noclose` metadata
- Define settings for a location with a `_settings.json` file
- Display the selection action as a shortcut with `actions.selection.location` metadata
- Fulscreen button in title bar
- Check for license update when approaching expiration
- Webview: meaningful icons for toggling touch interaction
- Webview: option to ignore ssl errors
- Catalog: allow the definition of filters on inexistant data
- Kiosk mode: start page UI improvements
- Removed Boogie Board support
- [FIX] Powerpoint rendering errors
- [FIX] Animation delay when swiching sources
- [FIX] Save dialog not updating correctly when pluging back an USB drive
- [FIX] Error when saving from a demo universe on Surface Hub
- [FIX] No name dispayed when using a custom universe source on an USB drive
- [FIX] 3D models in error when refreshing an universe
- [FIX] Empty pdf generated when sharing videos as single pdf
- [FIX] Incomplete account details for registered users without a license
- [FIX] Setting a source as default not does not apply immediately in some cases
- [FIX] Crash when leaving a project with a background video
- [FIX] Stickers displayed with wrong aspect ratio

### 2.0.47 - August 29, 2019
- [FIX] Interactive backgrounds not displayed

### 2.0.46 - August 27, 2019
- Integrated calculator
- Consolidated and clearer activation experience in tutorial and settings
- Pin and tape UI adjustements
- Kiosk mode: standby videos per source or universe
- Kiosk mode: universe opens automatically in single-universe scenarios
- Kiosk mode: side menu button leaves the project
- [FIX] Powerpoint file links always open in browser for Sharepoint configurations
- [FIX] Provisionned SharePoint/Teams locations cannot be set as default

### 2.0.45 - August 1, 2019
- Support for more presentation remotes
- [FIX] Writing on taped documents also moves them on Samsung Flip

### 2.0.44 - July 23, 2019
- Ensure a "Compositeur Digital UX" folder exists when adding a cloud location
- Kiosk mode in settings
- [FIX] Errors and rendering issues on some Powerpoint documents
- [FIX] Delay when opening documents on some devices

### 2.0.43 - July 18, 2019
- Navigation button in 360° videos
- Stickers can be added to notes
- SharePoint or Teams universe sources can be provisionned for all users in an organisation
- Web: cursor position propagated to javascript touch events
- Visual feedback when sharing documents on Surface Hub
- Default preview for 3D objects
- Faster opening of projects and universes from `cdux://` links
- New `cdux://openoraddsource` action for integration with Microsoft Teams
- [FIX] Error when changing color right after closing a document
- [FIX] Documents may lose their state when re-opened right after they were closed
- [FIX] Text files appear empty if their encoding is not UTF8
- [FIX] Default save destination not displayed on some devices
- [FIX] Crash when navigating templates in some universes
- [FIX] Loan and investment simulators unresponsive if `noChrome` is set
- [FIX] No investment simulator icon on Surface hub
- [FIX] Inverted vertical axis when navigating 360° videos
- [FIX] Cannot "throw" documents if they are already half outside the screen
- [FIX] Broken "other" option in forms
- [FIX] Error when closing some documents or notes

### 2.0.39 - June 19, 2019
- Microsoft Dynamics demo "One Insurance"
- [FIX] Catalog search view initialization error

### 2.0.38 - June 14, 2019
- Prevent accidental reveal of bottom bar
- Sendgrid option to add a BCC to the sender
- `cdux://` activation with "Any" provider to find an universe regardless of its location
- [FIX] Cannot export to a single pdf

### 2.0.37 - June 6, 2019
- App rating dialog can be definitively dismissed
- 3D object rendering mode options: normal, transparent and wireframe, see [3D objects](../organise_content/supported_content/3dobj.html#metadata-available)
- [FIX] Error when initializing some quiz pages
- [FIX] Cannot export documents with stickers
- [FIX] Powerpoint rendering issues
- [FIX] Empty site/team list when adding a SharePoint or Teams location

### 2.0.35 - May 28, 2019
- Stickers UI and export improvement
- Customisable side menu icon
- Hideable bottom bar dots
- Investment simulator
- Integrated stickers and templates
- Share with SendGrid
- `.cdurl`: inline metadata and web pages displayed in a webview by default
- Demo banking: simuinvest
- [FIX] Catalog: formatting and slider steps for value ranges under 10
- [FIX] Dynamics crmsearch view not updating
- [FIX] Free license refresh button

### 2.0.30 - May 15, 2019
 - Faster project preparation from cloud
 - [FIX] Quiz multiple values answer not updating project data
 - [FIX] Duplicate document action


### 2.0.29 - April 23, 2019
- Videos streamed from cloud on shared devices
- [FIX] `.cdurl` folder link with trailing '/' not recognized in cloud universes
- [FIX] Lighting causing 3D objects to appear all white
- [FIX] Empty notes appear in history
- [FIX] Locations listed twice

### 2.0.28 - April 18, 2019
- Confirm dialog on app exit
- Global touch ink in the palette side menu
- 360° video support
- video.mute meta
- Prompt for MS account if absent when opening a cdux protocol link
- [FIX] font alignment on some Powerpoint presentations
- [FIX] real estate demo links
- [FIX] cannot signout
- [FIX] shared `_meta.txt` file ignored for online sources	
- [FIX] crashes when loading 3ds model & panorama with no images
- [FIX] crashes when launching a quizz document page with a broken item link
- [FIX] cache cleared when removing a cloud source
- [FIX] Capturing a 3D model shows all the controls, even if navigation is not started
- [FIX] Default location is not selected after removing a location
- [FIX] sticked notes move when a document aspect ratio changes
- [FIX] cdux protocol not launching a synchronized source if user name in the link does not match logged in user

### 2.0.26 - April 5, 2019
- MP3 files support
-	In-app survey
-	Stickers/magnets
-	Annoted then closed document kept available in projects
- Catalog: search documents in current universe
- Catalog: text filter	
- Form and quizz ui improvements
- Web views opened from links inherit configuration
-	Import multiple files at once
- Faster project closing
- Open document exports in external apps
- Refresh button on universes and projects lists
- Cloud locations sorted by site/team then library/channel 
- [FIX] Initial camera position for 3D objects
- [FIX] Templates text values lost when opening project
- [FIX] Sticked notes and documents cropped on export
- [FIX] Subscription randomly forgotten

### 2.0.20 - March 6, 2019
- Customizable maximum catalog search results
- [FIX] Background color ignored for 3D models
- [FIX] Sidebar menu click responsiveness

### 2.0.19 - February 22, 2019
- [FIX] Powerpoint links with unescaped uri may open incorrect document
- [FIX] Catalog search criterias layout sometimes hide options

### 2.0.18 - February 19, 2019
- Video: auto close configuration, see [Advanced settings - Video](../organise_content/advanced_setting.html#video)
- CRM search improvements
- Loan simulator:  'Additional costs' slider and disclaimer, see [Advanced settings - Loan simulator](../organise_content/advanced_setting.html#loan-simulator)
- Select a default location from the settings page
- Long press / right click on a location to refresh or remove
- Deleted Sharepoint sources are automatically removed from locations
- Better project date grouping: day of week for last 7 days, then month for last 12 months, then year
- [FIX] powerpoint import errors

### 2.0.17 - February 11, 2019
- Open universe source upon 'Add location' or plugging in a USB drive
- [FIX] 'Ctrl+V' text sometimes imported as invalid url
- [FIX] blurry map for higher zoom levels in catalog filters
- [FIX] Error when editing budget in CRM forms
- [FIX] Removing imported documents deletes files even if project is not saved
- [FIX] 'Add local source' adds the source as an universe

### 2.0.14 - January 29, 2019
- Warn if document is used when removing from imported
- [FIX] Slideshow error introduced in 2.0.13

### 2.0.13 - January 28, 2019
- CRM search UI improvements
- [FIX] Report pptx template converted to pdf from o365
- [FIX] Cannot manipulate some templates with text input areas

### 2.0.12 - January 24, 2019
- Choose between a report or all attached documents when sharing a pinboard
- [FIX] 'To text' action not working in note templates
- [FIX] Powerpoint presentations not loading in some cases
- [FIX] catalog map results navigation
- [FIX] catalog combined filters updates with hidden filters

### 2.0.11 - January 23, 2019
- Document menu stays behind attached documents and notes.
- Restored missing touch eraser button
- [FIX] Document imported twice in some cases
- [FIX] Links to files with uppercase extensions not found
- [FIX] Setting video autoplay delay disables autoplay
- [FIX] 'To text' action results in ArgNullException when note has no text

### 2.0.10 - January 18, 2019
- Add support for PPSX file
- Handle navigation key commands (Left & Right) to navigate in a slideshow (the last touched slideshow receives the commands)

### 2.0.9 - January 17, 2019
- Navigation commands in 3D viewer and virtual tour viewer are always reachable when the item is in a corner.
- Slide capture command in a slideshow is always reachable when the item is in a corner.

### 2.0.8 - January 16, 2019
- From an empty universe, on a shared device (e.g. a SurfaceHub), it is now possible to add a cloud location to save your project directly from the save window.
- Improved search engine: zoom functions tuned in map view.
- [FIX] Fixed error when launching a Map without a token.

### 2.0.7 - January 11, 2019
- Exportable product sheets
- Toggle between map and list search results
- [FIX] Empty universe projects saved on selected location by default
- [FIX] Return to current location when leaving project
- [FIX] Restore project state when close/restart app
- [FIX] Fixed error when changing project location to OneDrive

[comment]: # (-	Support: [Boogie Board Sync](https://myboogieboard.com/products/sync) tablet)
### 2.0.4 - January 8, 2019
- Improved search engine: map view
- [FIX] Fixed store locations not updated after a connection to an Office 365 account
- [FIX] Fixed sorting of projects when changing store location

### 2.0.1 - December 31, 2018
- Connect to your Sharepoint libraries and Teams channels: access universes and store projects
- New start page UI: manage and navigate between store locations, connect to your Office 365 account
- New project save UI: dynamically add location
- Faster project loading
- Interactive forms: fill info using sliders, pictures, text box, etc.
- Microsoft Teams integration: list, create or open new project directly from a team channel.
- New document import experience
- Improved search engine: french region selector, dropdown, multi-levels search
- Support du Français
- [Web] Interact with Compositeur Digital UX, see  [Web pages](../organise_content/supported_content/web_page.html#interactions-with-compositeur-digital-ux)

### 1.5.10 - October 30, 2018
- Improved 3D objets manipulation
- PowerBI interaction similar to websites

### 1.5.8 - October 18, 2018
- 3D focus & lighting improvements, skybox support 
- Support for license-defined analytics policy
- Support for metadata files in universe sources (e.g. USB drive)
- Fixed orientation for some image files
- Fixed share single pdf

### 1.5.7 - October 5, 2018
- Product sheets
- Webview fix for long-running scripts

### 1.5.5 - September 18, 2018
- Fixed random crashes when displaying a video
- New video customization options, see [Advanced settings - Video](../organise_content/advanced_setting.html#video)
- Support for background video
- Fixed 3DS files support for untextured models
- Loan simulator rates made customizable, see [Advanced settings - Loan simulator](../organise_content/advanced_setting.html#loan-simulator)
- Fixed web view audio playing in background
- Web view capture support

### 1.5.2 - September 10, 2018
- Support for .sequence polygonal pois

### 1.5.1 - September 03, 2018
- Support for virtual tours navigation between scenes
- Support for 3D models (.obj, .3ds)
- Improved navigation in web folders on Surface HUB
- Include screen capture in single pdf exports
- The "zoom" document button fits the avalaible space
- Bug fixes and performance improvements

### 1.4.7 - August 7, 2018
- App screenshot feature (for computers running Windows 10 April 2018 update)
- Support for HTML folders
- Bug fixes and performance improvements

### 1.4.0 - June 21, 2018
- Support: Samsung Flip stylus
- Custom toolbox notes: ink to text conversion
-	New experience when launching Compositeur Digital UX for the first time
-	Speed-up launching time
-	Aras PLM demo

### 1.2.19 - May 14, 2018
-	Fix: documents sometimes lock after inking

### 1.2.18 - May 3, 2018
-	Windows 10 April 2018 Update support
-	Notes: ink to text conversion
-	Share: multiple selection
-	Share: single PDF option
-	Share: project file includes imported items
-	New « Creativity Meeting » and « Project Meeting » demos
-	Toolbox: better custom note UI
-	Bug fixes and performance improvements
- Annotate without stylus
- Full-screen action on documents


[Back to Documentation](../index.md)
