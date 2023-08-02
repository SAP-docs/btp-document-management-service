<!-- loio585d79d6406d467cbb423f64fe2a95ff -->

# Configuring SAP Document Management Service for Desktop Client

The SAP Document Management Service desktop app is delivered with a default configuration, which you can adjust using the settings described below.



<a name="loio585d79d6406d467cbb423f64fe2a95ff__context_N10014_N10011_N10001"/>

## Context

> ### Note:  
> The administrator can restrict the choices available to you.



## Procedure

1.  Right-click the Document Management Service tray icon \(![](images/SDM_Client_Service_Desktop_Icon_b0aa4d2.png) \) and choose *Settings* \(![](images/General_Settings_Menu_Icon_29ee5df.png)\).

2.  On the *General* tab, enter the following data.


    <table>
    <tr>
    <th valign="top">

    Field


    
    </th>
    <th valign="top">

    Possible Values


    
    </th>
    <th valign="top">

    Comment


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Language


    
    </td>
    <td valign="top">
    
    English \(United States\)


    
    </td>
    <td valign="top">
    
    The display language of the desktop app.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Autostart


    
    </td>
    <td valign="top">
    
    -   Selected checkbox \(default\)
    -   Unselected checkbox


    
    </td>
    <td valign="top">
    
    If you deselect *Autostart*, the app no longer starts automatically when the system is started.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Enable Logging


    
    </td>
    <td valign="top">
    
    -   Unselected checkbox \(default\)
    -   Selected checkbox


    
    </td>
    <td valign="top">
    
    You can activate logging. The desktop app then logs technical information in a log file on your computer. This might be helpful if you need to contact support. To access the log file, choose *Help* \> *Log File* from the context menu of the tray icon.

    > ### Note:  
    > The administrator can deactivate this setting centrally.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Show Taskbar Notifications


    
    </td>
    <td valign="top">
    
    -   Selected checkbox \(default\)
    -   Unselected checkbox


    
    </td>
    <td valign="top">
    
    You can activate the display of notifications in the taskbar \(Microsoft Windows desktop\) or Notification Center \(Mac\).


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Log Files


    
    </td>
    <td valign="top">
    
    10 \(default\)


    
    </td>
    <td valign="top">
    
    By default, 10 log files are generated for each user.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Root Folder


    
    </td>
    <td valign="top">
    
    <code><i class="varname">&lt;Drive&gt;</i>:\\<i class="varname">&lt;folder&gt;</i></code> \(Microsoft Windows\) or <code>:/<i class="varname">&lt;folder&gt;</i></code> \(Mac OS\)


    
    </td>
    <td valign="top">
    
    The location where you want to place your topmost Document Management Service folder.

    > ### Note:  
    > Moving the root folder outside of your protected user folder \(default\) can expose your documents to other users on this computer.

    > ### Note:  
    > Do not move your root folder to a network share. This share is not available if you are offline and not connected to the network. This means that your Document Management Service root folder is not available either.

    > ### Note:  
    > Do not move your root folder to a device running on a FAT32 file system. The desktop app uses extended file attributes \(Alternate Data Stream in Microsoft Windows\) for storing the object ID property. These extended file attributes are not supported in FAT32 file systems.

    To change the root folder location, open the file system using *Browse* and select a new folder location.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Synchronization


    
    </td>
    <td valign="top">
    
    -   Every 30 minutes
    -   Every 60 minutes
    -   Every 90 minutes
    -   Every 120 minutes


    
    </td>
    <td valign="top">
    
    The synchronization interval at which the app polls the server for content updates.

    You can set an interval for the *Repositories* folder.

    > ### Note:  
    > Your local changes are always synchronized with the server immediately.

    > ### Note:  
    > The administrator can restrict the choices available to you. In this case, only the intervals that are equal to or higher than the one set by the administrator are displayed. However, you can still choose *Sync Now* from the context menu of the tray icon to start the synchronization process manually.


    
    </td>
    </tr>
    </table>
    
3.  On the *Connection* tab, enter the following data.


    <table>
    <tr>
    <th valign="top">

    Field


    
    </th>
    <th valign="top">

    Possible Values


    
    </th>
    <th valign="top">

    Comment


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Server URL


    
    </td>
    <td valign="top">
    
    Server URL


    
    </td>
    <td valign="top">
    
    The URL of the server.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Bandwidth


    
    </td>
    <td valign="top">
    
    -   Do not limit \(default\)
    -   64 KB/s
    -   128 KB/s
    -   256 KB/s
    -   512 KB/s
    -   1024 KB/s


    
    </td>
    <td valign="top">
    
    The bandwidth at which the app transfers files during uploads or downloads. The bandwidth is not applied per transfer but is split among all transfers.

    If you are transferring large files, consider limiting the bandwidth of the app so that you can simultaneously browse the Internet, for example. On the other hand, a larger bandwidth allows faster uploads and downloads.

    > ### Note:  
    > The administrator can restrict the choices available to you.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Proxy


    
    </td>
    <td valign="top">
    
    -   No Proxy
    -   Automatically Detect Settings \(default\)
    -   Manual Configuration


    
    </td>
    <td valign="top">
    
    Defines how the app connects to the network. The setting *Manual Configuration* provides additional input fields for the host, proxy port, user, and password. The *User* and *Password* fields are optional.


    
    </td>
    </tr>
    </table>
    
4.  On the *Selective Sync* tab, select the folders you want to sync.

    All repositories are displayed, even if they are not reachable. If a repository cannot be reached, it is displayed in red.

    For more information, see [Synchronizing Selected Folders](synchronizing-selected-folders-23bbcdb.md).

5.  On the *Account* tab, to change the logon mode or the logged-on user, choose *Unlink Account*.

6.  Save your settings.

7.  Some of the changes require a restart to take effect. If a message is displayed informing you that this is the case, restart the application.


**Related Information**  


[Changing the Server or Switching the User](changing-the-server-or-switching-the-user-ad29610.md "You either use oAuth or user name and password plus the Remember Password setting to log on to your desktop app. To use a different logon mode or to log on with another oAuth user, you unlink your account.")

[Creating Files](creating-files-ab3b9b8.md "To synchronize files using the Document Management Service desktop app, store these files in your root folder.")

[Sharing Files or Folders](sharing-files-or-folders-452f0e1.md "You can share files or folders using the context menu of Document Management Service.")

[Creating New Empty Share](creating-new-empty-share-63606a2.md "You can create a new share directly in the desktop app.")

[Editing the Settings of a Share](editing-the-settings-of-a-share-6406d16.md "You can edit the settings of a share starting in the desktop application, which then opens the Web application.")

[Renaming a Share](renaming-a-share-fa5bc9d.md "You can rename a share using the Document Management Service context menu in your Explorer (Windows) or in Finder (Mac)..")

[Deleting a Share](deleting-a-share-c4d2860.md "You can delete a share directly in the desktop app.")

[Accessing SAP Document Management Service](accessing-sap-document-management-service-af38bd8.md "The SAP Document Management Service tray icon is your central access point for the desktop app, for example, to open files and folders, the settings page, and the notifications page.")

[Using Favorites](using-favorites-feb23bc.md "In the Document Management Service desktop app, you can view favorite files and folders that you have created in the Favorites folder using the Web app.")

[Checking Notifications](checking-notifications-0c0b57c.md "The desktop app displays notification popups, for example, if it recognizes synchronization or naming conflicts.")

[Checking the File Transfer Status](checking-the-file-transfer-status-0f0d9e8.md "")

[Synchronizing Files and Folders Manually](synchronizing-files-and-folders-manually-68edf8f.md "The files and folders in your local Document Management Service folder are periodically synchronized with the server, based on the settings you've made.")

[Synchronizing Selected Folders](synchronizing-selected-folders-23bbcdb.md "In the Document Management Service desktop app, you can define which folders are periodically synchronized to your local desktop app.")

[Displaying Recently Downloaded Files and Folders](displaying-recently-downloaded-files-and-folders-a28fbcb.md "After you have uploaded or deleted files in the Web or mobile apps of Document Management Service, you can view these changes as a list in the desktop app.")

[Versioning of Files](versioning-of-files-b22e616.md "The Document Management Service Desktop app enables you to create new versions of a file, and edit latest version of the file. Versioning in Document Management Service is also helpful for teamwork, where you're collaborating with colleagues on projects and the content goes through several iterations of improvement and review. This way, you can track the file history and the development of the final version.")

[Solving Synchronization Conflicts](solving-synchronization-conflicts-eb04b7b.md "The Document Management Service desktop app recognizes if two files are in conflict and displays a notification.")

[Sending Mail Attachments Using the Microsoft Outlook Add-In](sending-mail-attachments-using-the-microsoft-outlook-add-in-a5f77e4.md "Document Management Service offers a Microsoft Outlook add-in that can automatically create a share, include a link to the share in your mail or meeting request, and store the files you want to attach to your mail or meeting request in this share. In this way, you can attach files that exceed your allowed mail attachment size limit.")

[Selecting File or Folder in Web App](selecting-file-or-folder-in-web-app-ccc68dc.md "You can use your Document Management Service desktop app to display any item from the Document Management Service folder in the Web app.")

[Downloading the Latest Version of the Desktop App](downloading-the-latest-version-of-the-desktop-app-7c849bd.md "You can easily access the download location that your administrator has preconfigured for the Document Management Service desktop app.")

[Copying the Link to a File or Folder](copying-the-link-to-a-file-or-folder-3d28fed.md "You can copy the link to any file or folder of your Document Management Service desktop app to the clipboard of your device.")

[Requesting Support](requesting-support-2fba81d.md "You can create an incident to the team responsible for advice on the desktop app.")

[Modern UI How-Tos](modern-ui-how-tos-fe00e02.md "The following sections introduce the features of the Document Management Service Modern UI.")

