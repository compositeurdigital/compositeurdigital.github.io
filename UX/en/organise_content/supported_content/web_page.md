# Web Pages

## Summary
* [Actions within Compositeur Digital UX](#actions-within-compositeur-digital-ux)
* [Content extensions](#content-extensions)
  * [I want to display a web site link which will be opened in a web browser](#i-want-to-display-a-web-site-link-which-will-be-opened-in-a-web-browser)
  * [I want to display an external web site inside my Compositeur Digital UX](#i-want-to-display-an-external-web-site-inside-my-compositeur-digital-ux)
  * [I want to display local HTML content](#i-want-to-display-local-html-content)
* [Interactions with Compositeur Digital UX](#interactions-with-compositeur-digital-ux)
* [Summup](#summup)
* [Metadata available](#metadata-available)
* [Download a sample](#download-a-sample)

## Description

This content allows you to display a local html content, or a web site page inside your Compositeur Digital UX. Web site pages can also be displayed as links, so that when they are selected, an external web browser is showing them.

To interact with a web page, press the navigation button at the center of the item: This will trigger the navigation mode.

![Web page navigation mode enabled](../../img/content_web_page_start.JPG)

In navigation mode, you can interact with the content displayed in webview in the same manner as you would do on a web browser. However, the manipulation actions (move, zoom, rotate) you can ordinary use on all documents are disabled (unless you touch the document on its top bar, where the website name is written). Press the `end navigation` button (next to the action button) to end navigation.

![Web page navigation mode disabled](../../img/content_web_page_end.JPG)

To navigate back in history, press the arrow in the top left corner. 
To directly go to the home page, press the `Home` button in the webview's menu.

## Actions within Compositeur Digital UX

Web page items support the following action. To have a complete overview of each action, [see the section Actions](actions.md)

**Actions menu**

| Annotate | Capture  | Duplicate |Open in native app | Save as  | Selection | Share    | 
|:--------:|:--------:|:---------:|:-----------------:|:--------:|:---------:|:--------:|
| &#x2716; | &#x2716; | &#x2714;  | &#x2716;          | &#x2716; | &#x2714;  | &#x2716; |

**Interaction with the item**

| Navigation Mode | Web page navigation |
|:---------------:|:--------------------|
| &#x2714;        | &#x2714;            |

## Content extensions

Depending on your goal, you have several content extensions which can be used.

### I want to display a web site link which will be opened in a web browser

To display a web site link which will be opened in a web browser, create a file named `<NameOfMySite>.cdurl`. Inside this file, add a line :
`url = <UrlOfMyWebsite>`,  e.g, `url = https://www.msn.com/en-us/`

![Web browser link](../../img/content_web_page_link_folder.JPG)

### I want to display an external web site inside my Compositeur Digital UX

To display a web site inside your Compositeur Digital UX, you need a `.cdurl` file, and a `meta` file. Metadata are very useful to customize the way your Compositeur Digital UX acts. [Check the metadata section for more information](../advanced_setting.md).


![Compositeur Digital UX Web viewer](../../img/content_web_page_cdux_folder.JPG)

### I want to display local HTML content

To display local HTML content, create a folder and add the extension `.html` or `.web` at the end of the name of your folder. Inside your `web` folder, you can use `css`, `htm`, `html` and `js` files. You can use images as well.

If you have several `html` files inside this folder, by default, Compositeur Digital UX will look for a file named `index.hmtl`. If no such file can be found, the starting file will be the first regarding the alphabetical order.

![Local HTML content](../../img/content_web_page_local_folder.JPG)

### Interactions with Compositeur Digital UX

With html contents, you can have interaction between your webpage an Compositeur Digital UX using javascript.
All actions are available through the object `CDUX`. All 'get' operations are asynchronous.

**openItem**(string path)
<br />open an item from your universe by giving its relative path from your webview
<br />`<a href="javascript:CDUX.openItem('../image.jpg');">open image</a>`
<br />`<a href="javascript:CDUX.openItem('2ndPage.html?name=test');">open new webview</a>`

**importItem**(string base64, string filename)
<br />import and open binarydata as a file in the current project
```javascript
var pdf = new jsPDF();
/* generate a pdf */
var byteArray = pdf.output('arraybuffer');
CDUX.importItem(window.btoa(byteArray), 'My File.pdf');
```
**SetJsonProjectData**(string dataKey, string value)
<br />store the value (primitive or complex object) in the project under the given key

**async getJsonProjectData**(string datakey)
<br />retrieve the value stored in the project under the given key

**setJsonInstanceData**(string dataKey, string value)
<br />store the value (primitive or complex object) in the webview instance under the given key

**async getJsonInstanceData**(string dataKey)
<br />retrieves the value stored in the webview instance under the given key

**async getJsonUniverseData**(string dataKey)
<br />retrieves the value stored in universe data under the given key

**async getJsonInstanceDataFor**(string instanceId, string dataKey)
<br />retrives the value stored in the instance having instanceId under the given key

**registerProjectDataChangedCallback**(string dataKey, string callBackFunctionName, bool sendNewValueAsArgument)
<br />subscribe to project data changes at the given key. Each time the value is changed (or a subvalue of the given key) the function given in parameter is called, with or without sending the new value as parameter.

**unRegisterProjectDataChangedCallback**(string dataKey)
<br />unsubscribe to the project changes for this key

**registerInstanceDataChangedCallback**(string dataKey, string callBackFunctionName, bool sendNewValueAsArgument)
<br />subscribe to instance data changes at the given key. Each time the value is changed (or a subvalue of the given key) the function given in parameter is called, with or without sending the new value as parameter.

**unRegisterInstanceDataChangedCallback**(string dataKey)
<br />unsubscribe to the instance changes for this key

**project and Instance Data**
<br />Project Data are shared with all other documents whereas Instance Data only concerns the current instance of your document (Note that InstanceData will be copied in case you duplicate the webview).
With ProjectData you can interact with with the values of an other webview, but also of a [Quiz](quiz.md), a [Form](form.md) or a [Mortgage simulator](simulator.md)

**async getCurrentItem**(bool includeMetadata, bool includeResources)
<br />returns information (item's relative path to the webView, item's preview & icon relative path, if any) about the current item.

**async findItems**(string relativePath, bool includeMetadata, bool includeResources)
<br />return information about the item matching the relative path (relative path, preview & icon path if any, item's content).

**clearWorkspace**(bool keepInstance)
<br />clears the workspace. If keep instance is true, the web view will stay in the workspace.

**setCurrentPage**(string pageId)
<br />change the current instance page

**async getCurrentPage**
<br />returns the current instance page id

**async getCurrentInstance**
<br />returns the current instance id

**async getCurrentSelection**
<br/>returns all the id of the instances that are part of the user's selection.

**openInstance**(string instanceId)
<br />opens the instance in the workspace

**examples**
```javascript
    var objectValue = { 'name': 'Marc Dupont', 'phoneNumber': '06 12 24 49 33' }
    CDUX.setJsonProjectData('school.director', JSON.stringify(objectValue));
    
    //to retrieve later this value use :
    var director = JSON.parse(await CDUX.getJsonProjectData('school.director'));
    
    //if you only want to get the name, you can also use a more precise key :
    var directorName = JSON.parse(await CDUX.getJsonProjectData('school.director.name')) ;
    
    //to be warn of a change of phoneNumber :
    function phoneChanged() { }
    CDUX.registerProjectDataChangedCallback('school.director.phoneNumber', phoneChanged.name, false);
    
    //to be warn of a any change inside director's object :
    function infoChanged() { }
    CDUX.registerProjectDataChangedCallback('school.director', infoChanged.name, false);
```

**Deprecated** *: the below methods are kept only for legacy reasons
<br />getProjectData: retrieve a value stored on the current project by giving its key
<br />`var budget = CDUX.getProjectData("firstName");`
<br />setProjectData: sets a value on the current project for a given key
<br />`CDUX.setProjectData("finance.budget", 600000);`
<br />getInstanceData: retrieve a value stored on the current page instance by giving its key
<br />`var value = CDUX.getInstanceData("questionnay.thirdAnswer");`
<br />setInstanceData: sets a value on the current page for a given key
<br />`CDUX.setInstanceData("questionnay.thirdAnswer", "Yes");`*


### Summup

|          | Web site link (web browser) | Web site (CDUX)   | Local Html content       |
|----------|:----------------------------|:------------------|:-------------------------|
|Extensions| `cdurl`                     | `cdurl`           | Folder `.html` or `.web` |

## Metadata available

Metadata will help you to customize the way your web viewer behaves.

| Metadata Key                      | Value               | Description                                                                 |
|:---------------------------------:|:-------------------:|:----------------------------------------------------------------------------|
| `table.viewer`                    | cdux                | Makes sure the `cdurl` link will be displayed inside Compositeur Digital UX |
| `table.viewer`                    | extern              | Makes sure the `cdurl` link will be displayed outside Compositeur Digital UX |
| `web.manipulationMode`            | `toggle` or `integrated`| If `toggle`, all touch movements acts only on the container until the user enable navigation mode, then all interactions are transmited to the web content. If `integrated`, single taps are transmited to web content whereas more complex touch movements (slide, zoom, ...) will move the container  |
| `action.manipulation.location`    | `shortcut` or undefined   | Controls where the manipulation invite appears when manipulation mode is set to `toggle`. Set to `shortcut` to display in the bottom right corner, leave undefined for the default centered button |
| `web.showChrome`                  | True of False       | If true, a navigation bar at the top of the view will be shown. Else, no navigation bar will be displayed. |
| `web.viewport.width`              | 1000 (number)       | Sets the default width of the view.                                         |
| `web.viewport.height`             | 800 (number)        | Sets the default height of the view.                                        |
| `web.nossl`                       | True or False       | Allow navigation to pages that have untrusted certificates.                 |
| `web.newWindowOnNavigation`       | True or False       | Open all links in a new windows                                             |
| `web.newWindow.*`                 | -                   | Any metadata with the `web.newWindow` prefix will be applied to new windows opened from the current page. If no such metadata is set, the current metadata will be used. |  

[Access common metadatas](../advanced_setting.md#summary)

By default , `cdurl` link have the metadata `web.manipulationMode` set to 1 and the metadata `web.showChrome` set to True.

Folders with the extension `.web` or `html` have the metadata `web.manipulationMode` set to 0 and the metadata `web.showChrome` set to False.

Navigation Mode to 1 (left) and 0 (right)

![Navigation mode 1 (left) vs 0 (right)](../../img/content_web_page_manipulationMode.JPG)

ShowChrome True (left) and ShowChrome False (right)

![ShowChrome true (left) vs false (right)](../../img/content_web_page_showChrome.JPG)

## Download a sample

A Demo Universe which contains samples for web page contents is available, [give it a try!](../Demo-Universe.zip) &#x1f604;

Next : [Forms](form.md)

[Back to Supported Content](index.md)
