<!-- loioa5f77e4b10bb4700907576c4afa05caa -->

# Sending Mail Attachments Using the Microsoft Outlook Add-In

Document Management Service offers a Microsoft Outlook add-in that can automatically create a share, include a link to the share in your mail or meeting request, and store the files you want to attach to your mail or meeting request in this share. In this way, you can attach files that exceed your allowed mail attachment size limit.



## Prerequisites

-   You're a named user of the Document Management Service solution.
-   You've installed and configured the Document Management Service desktop app for Microsoft Windows including the Microsoft Outlook add-in for Document Management Service.
-   You use oAuth authentication to log on to your Document Management Service desktop app.

    The Microsoft Outlook add-in automatically detects the settings for the server URL and the authentication data you used for the desktop app.

-   You use Microsoft .NET Framework 4.5.2.
-   You use Visual Studio Tools for Office \(VSTO\) Runtime. If the add-in is installed for use with Microsoft Outlook 2010, then installing the redistributable version of VSTO 4.0 is mandatory.

    You can download the VSTO runtime from the Microsoft Web page at [https://www.microsoft.com](https://www.microsoft.com), either for the 32-bit edition or the 64-bit edition.

    Microsoft Office 2013 already has the latest VSTO runtime and you may not be required to install it explicitly.




## Procedure

1.  In Microsoft Outlook, check that the *Doc Management On/Off* button is set to active in the Document Management Service add-in.

    It's set to active by default.

2.  In Microsoft Outlook, go to the add-in settings for sending attachments by choosing the *Settings* button.


    <table>
    <tr>
    <th valign="top">

    Setting
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Minimum File Size for Attachments* 
    
    </td>
    <td valign="top">
    
    Defines the minimum file size of attachments that you want to send using Document Management Service. The default value is 5 MB. You can decrease or increase it if you want.
    
    </td>
    </tr>
    </table>
    
3.  Save your settings.

4.  Create your mail or meeting request as usual.

5.  Attach or drag and drop the files to send with the mail or meeting request.

    If the attachment size exceeds the allowed limit, a popup window appears to inform you that your mail will be sent using Document Management Service. You can confirm this action or cancel it.

6.  On the *Create Share* screen, enter a name and choose the access settings of your share by completing the form for share creation.


    <table>
    <tr>
    <th valign="top">

    Option
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Anyone with the link has access
    
    </td>
    <td valign="top">
    
    Creates a public share and anyone with the link can access it.

    > ### Tip:  
    > -   You can set write permission, modify the expiration period, and restrict the share access using a password.
    > 
    > -   If you've given recipients write access, they can choose to store their attachments in the same shared folder when they reply or forward a mail or a meeting request, and attach files to the message.
    > 
    > -   If the expiration period times outand you haven't defined a date for automatic deletion, the share won't be removed.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Share with members
    
    </td>
    <td valign="top">
    
    Creates a share that can be accessed only by users with authentication in Document Management Service.

    > ### Tip:  
    > You can specify a member's role as *Reader* or *Contributor*.


    
    </td>
    </tr>
    </table>
    
7.  Choose *Create* to trigger the share creation with the above settings.

    To delete your newly created share, choose *Delete*.

8.  \(Optional\) To upload more files, choose *Upload File* or simply drag and drop them in the *<Upload Files\>* field.

    To remove a file that has already been added, use the *X* button next to the file name.

9.  Choose the *Back to Message* button to go back to your mail.

10. Send your mail by choosing *Send*.




## Results

Document Management Service creates a share. Its name is either the mail subject or the name you gave to the share upon its creation. In addition, a link to this share is created and inserted into the mail, together with a list of attached documents. As creator of the new share, you can access it in the repository that is collaboration enabled.

> ### Note:  
> -   If you've selected the *Anyone with the link has access* option, the share is available as a public link in the share that is part of a collaboration-enabled repository.
> 
> -   If you've selected the *Share with Members* or *Anyone with the link has access* together with *Share with Members* options, the share is available as a shared folder in collaboration-enabled repositories.

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

[Synchronizing Selected Folders](synchronizing-selected-folders-23bbcdb.md "In the Document Management Service desktop app, you can define which folders are periodically synchronized to your local desktop app.")

[Displaying Recently Downloaded Files and Folders](displaying-recently-downloaded-files-and-folders-a28fbcb.md "After you have uploaded or deleted files in the Web or mobile apps of Document Management Service, you can view these changes as a list in the desktop app.")

[Versioning of Files](versioning-of-files-b22e616.md "The Document Management Service Desktop app enables you to create new versions of a file, and edit latest version of the file. Versioning in Document Management Service is also helpful for teamwork, where you're collaborating with colleagues on projects and the content goes through several iterations of improvement and review. This way, you can track the file history and the development of the final version.")

[Solving Synchronization Conflicts](solving-synchronization-conflicts-eb04b7b.md "The Document Management Service desktop app recognizes if two files are in conflict and displays a notification.")

[Selecting File or Folder in Web App](selecting-file-or-folder-in-web-app-ccc68dc.md "You can use your Document Management Service desktop app to display any item from the Document Management Service folder in the Web app.")

[Downloading the Latest Version of the Desktop App](downloading-the-latest-version-of-the-desktop-app-7c849bd.md "You can easily access the download location that your administrator has preconfigured for the Document Management Service desktop app.")

[Copying the Link to a File or Folder](copying-the-link-to-a-file-or-folder-3d28fed.md "You can copy the link to any file or folder of your Document Management Service desktop app to the clipboard of your device.")

[Requesting Support](requesting-support-2fba81d.md "You can create an incident to the team responsible for advice on the desktop app.")

[Modern UI How-Tos](modern-ui-how-tos-fe00e02.md "The following sections introduce the features of the Document Management Service Modern UI.")

