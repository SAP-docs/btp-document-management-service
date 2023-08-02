<!-- loio23bbcdbb3be749b69c739f60c202b2de -->

# Synchronizing Selected Folders

In the Document Management Service desktop app, you can define which folders are periodically synchronized to your local desktop app.



## Context

If you expand a node in the folder tree, the availability of the folders in this node is checked. If the desktop app can't connect to a folder, the folder name is displayed in red along with a message \(not reachable\). The reason can be a network problem or a problem with the configuration of this repository.



## Procedure

1.  In the context menu of the tray icon \(![](images/SDM_Client_Service_Desktop_Icon_b0aa4d2.png)\), choose *Selective Sync* \(![](images/Menu_Selective_Sync_e644379.png)\).

2.  On the *Selective Sync* tab, select the folders you want to sync.

    > ### Note:  
    > The administrator can restrict the choices available to you.
    > 
    > All files and subfolders of a folder marked for sync are synced. You cannot choose to sync only the subfolders or only the files.If you select only a subfolder, only the contents of this subfolder are synced and not the complete repository.
    > 
    > By default, the selection of *Documents* in the *Selective Sync* tree is disabled. If you selected *Documents* for sync in a previous version of the desktop app and upgrade to new one, then the *Corporate Documents* selection is removed and all repositories beneath this node are marked for selective sync. If the administrator has enabled sync on *Repositories* root node, you can select the *Repositories* for sync.




## Results

The selected folders are synced with the file system. Deselecting folders on the *Selective Sync* tab doesn't automatically delete the folders from the file system. However, you can remove the folders by confirming the popup that appears, or by deleting the folders directly from the file system later on.

In Microsoft Windows: If the folder marked for sync that you want to delete contains subfolders, you've to delete the subfolders before deleting the parent folder.

If you want to rename or delete a subfolder marked for sync, the parent folder needs to be marked for synchronization as well.

**Related Information**  


[Configuring SAP Document Management Service for Desktop Client](configuring-sap-document-management-service-for-desktop-client-585d79d.md "The SAP Document Management Service desktop app is delivered with a default configuration, which you can adjust using the settings described below.")

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

[Displaying Recently Downloaded Files and Folders](displaying-recently-downloaded-files-and-folders-a28fbcb.md "After you have uploaded or deleted files in the Web or mobile apps of Document Management Service, you can view these changes as a list in the desktop app.")

[Versioning of Files](versioning-of-files-b22e616.md "The Document Management Service Desktop app enables you to create new versions of a file, and edit latest version of the file. Versioning in Document Management Service is also helpful for teamwork, where you're collaborating with colleagues on projects and the content goes through several iterations of improvement and review. This way, you can track the file history and the development of the final version.")

[Solving Synchronization Conflicts](solving-synchronization-conflicts-eb04b7b.md "The Document Management Service desktop app recognizes if two files are in conflict and displays a notification.")

[Sending Mail Attachments Using the Microsoft Outlook Add-In](sending-mail-attachments-using-the-microsoft-outlook-add-in-a5f77e4.md "Document Management Service offers a Microsoft Outlook add-in that can automatically create a share, include a link to the share in your mail or meeting request, and store the files you want to attach to your mail or meeting request in this share. In this way, you can attach files that exceed your allowed mail attachment size limit.")

[Selecting File or Folder in Web App](selecting-file-or-folder-in-web-app-ccc68dc.md "You can use your Document Management Service desktop app to display any item from the Document Management Service folder in the Web app.")

[Downloading the Latest Version of the Desktop App](downloading-the-latest-version-of-the-desktop-app-7c849bd.md "You can easily access the download location that your administrator has preconfigured for the Document Management Service desktop app.")

[Copying the Link to a File or Folder](copying-the-link-to-a-file-or-folder-3d28fed.md "You can copy the link to any file or folder of your Document Management Service desktop app to the clipboard of your device.")

[Requesting Support](requesting-support-2fba81d.md "You can create an incident to the team responsible for advice on the desktop app.")

[Modern UI How-Tos](modern-ui-how-tos-fe00e02.md "The following sections introduce the features of the Document Management Service Modern UI.")

