# Administrative Guide

Follow this guide to learn how you can manage your Compositeur Digital UX administrative data : license, Office365 connection, Compositeur Digital folders...

## Summary

* [Compositeur Digital UX license](#compositeur-digital-ux-license)
  * [Sign-in](#sign-in)
  * [Sign-out](#sign-out)
* [Office365 account](#office365-account)
  * [Office365 Sign-in](#office365-sign-in)
  * [Office365 Sign-out](#office365-sign-out)
  * [Microsoft Teams](#add-microsoft-teams)
  * [SharePoint sites](#add-sharepoint-sites)
* [Add local folders](#add-local-folders)
* [USB Keys](#usb-keys)
* [Kiosk mode](#kiosk-mode)

## Compositeur Digital UX license

The Compositeur Digital UX offers a preview mode with a limited set of features without account creation. 

If you have an existing Compositeur Digital license please follow the description below to sign in from the application. 

Alternatively, you can create an account [here](http://www.compositeurdigital.com/Account/Register) and [contact us](mailto:contact@excense.fr) or purchase a license.


### Sign-in

![1. Sign in part 1](../img/administrative_signin1.JPG)

1. On the app start page, click on the `Settings` button.

![1. Sign in part 2](../img/administrative_signin2.JPG)

2. On the settings page, click on `Add license`, under `Compositeur Digital license`.
1. Enter your username and password and click on `Sign in`.
1. You're connected! Your name and license type appears under `Compositeur Digital license`. 


**Note** : The device will store your credentials. Compositeur Digital UX will use the last signed-in account anytime you start a new session. If you have installed Compositeur Digital UX on a shared device, like a Microsoft Surface Hub, once you have linked a Compositeur Digital license to the device, you won't be able to remove the license unless you [contact our support team](mailto:support@excense.fr)

### Sign-out

At any time, you can freely decide to sign out.

1. On the app start page, click on the `Settings` button.
1. On the settings page, click on your name under `Compositeur Digital license`, then click on `Sign out`.

## Office365 account

Compositeur Digital UX allows you to directly sign in to your Office365 tenant. Doing so, you can stream content from your SharePoint libraries, or Microsoft Teams channels and work on a device that does not have your documents downloaded.

**Note** : This way of accessing your documents requires that you have an internet connection available each time you request your streamed universe.

### Office365 Sign in

![1. Sign in office365 part 1](../img/administrative_signin_o365.JPG)

1. On the app start page, click on the `Connect...` button. 
1. Follow the Office365 sign in instructions.
1. You're connected.

### Office365 Sign out

![1. Sign out office365](../img/administrative_signout_o365.JPG)

1. On the app start page, click on your Office 365 account.
1. Click on `Sign out`.

### Add Microsoft Teams channels

Once your Office365 account has been added, you can access content from your Microsoft Teams channels. To do so, you have to create a `Compositeur Digital UX` folder inside your channel. 

![Microsoft Teams](../img/administrative_teams.jpg)

In the screenshot above, i have a Team called `Mon canal teams`, with a channel called `General`. Inside the `General` channel files, i have created a folder `Compositeur Digital UX`. This folder contains universes. 

From my Compositeur Digital UX app, I can stream this library.

**Note** : Your channel must contain a `Compositeur Digital UX` folder at its root.

![Microsoft Teams : add location](../img/administrative_add_teams_site.jpg)

1. On the app start page, click on your `Add location...`
1. Click on `Teams or SharePoint library`.

![Microsoft Teams : select channel](../img/administrative_add_teams_site2.jpg)

3. Enter the name of your Teams.
1. Pick the Teams channel amongst the proposed choices
1. Click on `Add`.

![Microsoft Teams : channel added](../img/administrative_add_teams_site3.jpg)

6. The source has been added to your sources list. 

### Add SharePoint sites

Let's take another example. I have a SharePoint site called `My site`. Under this site, I have a `Documents` library. Inside this library, I have a folder called `Compositeur Digital UX`, which contains universes. 

**Note** : Your site's library must contain a `Compositeur Digital UX` folder at its root.

![SharePoint](../img/administrative_sharepoint.jpg)

1. On the app start page, click on your `Add location...`
1. Click on `Teams or SharePoint library`
1. Enter the name of your SharePoint site.
1. Pick the name of the library that contains a `Compositeur Digital UX` folder.
1. Click on `Add`.
1. The source has been added to your sources list. 

![SharePoint : site added](../img/administrative_add_sharepoint.jpg)


## Add local folders

By default, your universes are all stored under a single folder of your personal computer. This folder is `<HD>\<username>\Documents\Compositeur Digital UX`.

Depending on your enterprise configuration, you could have an access to a shared storage system (e.g. Microsoft SharePoint, Google Drive, Dropbox, ect). You can add these folders as Compositeur Digital folders. It means that when you start Compositeur Digital UX, the system will check if there are universes in all the folders you have set.

Using a shared storage system is very convenient to share your universes with all the people who need to use Compositeur Digital UX.

To add existing Compositeur Digital folders:

![Add local folders](../img/administrative_add_cd_folders.JPG)

1. On the app start page, click on `Add location...`
1. Click on `Local folder`
1. Pick your folder.
1. That's all &#x1F604;

## USB Keys

When you connect a USB key to your device, Compositeur Digital UX wil automatically check if the USB Key contains a `Compositeur Digital UX` folder at its root. If there is such a folder, a source will automatically be added.

![Usb sources](../img/administrative_usb_keys.JPG)

## Kiosk Mode

A kiosk mode is available in the app. This mode is adapted to device which are used as a public terminal. 

When the kiosk mode is enabled, it reduces the actions which can be triggered in Compositeur Digital UX : the user can only open a universe and annotate documents. Saving is disabled, and sharing actions as well. It is not possible to import documents, or to create a selection. Blanksheets and notes are not available.  

### Setting up kiosk mode

The kiosk mode can be enabled or disabled from the settings menu. On the start page, click on `Settings` or press `F5`.

![Enable kiosk mode](../img/administrative_kiosk_activation.JPG)

1. Enable or disable kiosk mode.
2. After the specified period of inactivity, the application will reset and come back to the start page. See below to set up a [standby video](#standby).

![Kiosk mode start](../img/administrative_kiosk_start.JPG)

The start page presents a reduce set of actions. Only one source is visible, and the projects view is not available. 

![Kiosk mode workspace](../img/administrative_kiosk_workspace.JPG)

The workspace has a limited set of functions available. The side menu allows you to change the ink or the quit the workspace. Selection is not available, and import functions are disabled too. 

### Standby

After the period of inactivity specified the application can play a fullscreen video before resetting to the start page.
The video will play in a loop until the users interact with the application.

Set up a single video by naming the file `_standby` (eg: `_standby.mp4`) or a sequence of multiple videos by creating a folder named `_standby` containing video files. 

-  When resetting from the start page, the video(s) found in the current location will be used.

    ![Standby video in source](../img/administrative_standby_source.jpg)
-  When resetting from the workspace, the video(s) in the current universe will be used if they exist, otherwise the video(s) from the universe's location will be used.

    ![Standby video in universe](../img/administrative_standby_universe.jpg)


[Back to Documentation](../index.md)
