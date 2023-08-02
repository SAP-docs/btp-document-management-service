<!-- loioaf38bd8247074e99a0a5a9e5965a8edc -->

# Accessing SAP Document Management Service

The SAP Document Management Service tray icon is your central access point for the desktop app, for example, to open files and folders, the settings page, and the notifications page.



<a name="loioaf38bd8247074e99a0a5a9e5965a8edc__context_N10015_N10012_N10001"/>

## Context

You access the functions of the desktop app by using the context menu of this tray icon \(![](images/SDM_Client_Service_Desktop_Icon_b0aa4d2.png)\).



## Procedure

To open the context menu using Microsoft Windows, right-click the tray icon \(![](images/SDM_Client_Service_Desktop_Icon_b0aa4d2.png)\). With Mac OS, left-click the icon to open the context menu.

All files and folders stored in the local Document Management Service home folder are synchronized across all your devices where SAP Document Management Service is installed.

> ### Note:  
> In the desktop app, each folder and file has an icon that indicates its synchronization status.
> 
> -   No icon: The file or folder hasn't yet been synchronized.
> -   Blue arrows \(![Desktop App Sync Icon](images/Desktop_App_Sync_Icon_b42d16f.png)\): The file or folder is currently being synchronized.
> -   Green checkmark \(![Desktop App Sync Icon 2](images/Desktop_App_Sync_Icon_2_2f51941.png)\): The file or folder has been synchronized but might not be up to date if you're offline.
> -   Red x \(![](images/Error_Icon_Desktop_52588c3.png)\): The file or folder wasn't synchronized.

Changes made by other SAP Document Management Service apps are displayed in the desktop app as popup messages above the tray icon.



<a name="loioaf38bd8247074e99a0a5a9e5965a8edc__result_N10031_N10012_N10001"/>

## Results

The context menu provides the following options:

-   ![](images/SDM_Client_Service_Desktop_Icon_b0aa4d2.png)*Open Document Management Service Folder*

    Opens your SAP Document Management Service folder on your hard disk. \(Alternatively, double-click the tray icon to open the folder.\)

-   Information on space usage
-   ![](images/Menu_Sync_Now_Icon_e82d613.png)*Sync Now*

    Triggers a full synchronization of all your data. For more information, see [Synchronizing Files and Folders Manually](https://help.sap.com/viewer/ba2adb991f6e4b6a857e9f76a99402bd/Cloud/en-US/a3a33ce014004b789de2eb33760fb2b6.html "The files and folders in your local SAP Document Center folder are periodically synchronized with the server, based on the settings you have made.") :arrow_upper_right:.

-   ![](images/General_Settings_Menu_Icon_29ee5df.png)*Settings*

    Accesses the app settings. For more information, see [Configuring SAP Document Management Service for Desktop Client](configuring-sap-document-management-service-for-desktop-client-585d79d.md).

-   ![](images/Menu_Selective_Sync_e644379.png)*Selective Sync*

    Accesses the *Selective Sync* settings. For more information, see [Configuring SAP Document Management Service for Desktop Client](configuring-sap-document-management-service-for-desktop-client-585d79d.md).

-   ![](images/Menu_Upload_and_Download_15875c1.png)*Uploads and Downloads*

    Displays the upload and download progress. For more information, see [Checking the File Transfer Status](checking-the-file-transfer-status-0f0d9e8.md).

-   ![](images/Menu_Notifications_Icon_90185e7.png)*Notifications*

    Accesses the notifications. For more information, see [Checking Notifications](checking-notifications-0c0b57c.md).

-   ![](images/Menu_Help_Icon_301cef4.png)*Help*

    Groups the following items: accessing the online documentation, requesting support by e-mail, downloading the latest desktop app, accessing the app's log file, and viewing the version information.

-   ![](images/Menu_Log_On_Icon_74d9f74.png)*Log On*

    Logs you on to the desktop app, displaying the disconnected-from-server icon \(![](images/SDM_Desktop_Client_Application_Status_Disconnected_2951282.png)\) until the server is reached. On the logon screen, select whether to log on using your client certificate or your user name and password.

-   ![](images/Menu_Log_Off_Icon_ee35401.png)*Log Off*

    Logs you off from the desktop app, changes the tray icon to the logged-off status \(![](images/SDM_Desktop_Client_Application_Status_Disconnected_2951282.png)\), and stops synchronizing your content. You need to log off, for example, to change your password or to change your logon method, for example, from certificate to basic authentication.

-   ![](images/Menu_Exit_Icon_2c00e7e.png)*Exit*

    Ends the desktop app and removes the tray icon.


**Related Information**  


[Configuring SAP Document Management Service for Desktop Client](configuring-sap-document-management-service-for-desktop-client-585d79d.md "The SAP Document Management Service desktop app is delivered with a default configuration, which you can adjust using the settings described below.")

[Changing the Server or Switching the User](changing-the-server-or-switching-the-user-ad29610.md "You either use oAuth or user name and password plus the Remember Password setting to log on to your desktop app. To use a different logon mode or to log on with another oAuth user, you unlink your account.")

[Creating Files](creating-files-ab3b9b8.md "To synchronize files using the Document Management Service desktop app, store these files in your root folder.")

[Sharing Files or Folders](sharing-files-or-folders-452f0e1.md "You can share files or folders using the context menu of Document Management Service.")

[Creating New Empty Share](creating-new-empty-share-63606a2.md "You can create a new share directly in the desktop app.")

[Editing the Settings of a Share](editing-the-settings-of-a-share-6406d16.md "You can edit the settings of a share starting in the desktop application, which then opens the Web application.")

[Renaming a Share](renaming-a-share-fa5bc9d.md "You can rename a share using the Document Management Service context menu in your Explorer (Windows) or in Finder (Mac)..")

[Deleting a Share](deleting-a-share-c4d2860.md "You can delete a share directly in the desktop app.")

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

