<!-- loio8ea949d82ae3441ea033ad1e4bbbae94 -->

# Defining the App Settings \(iOS\)

You can define global settings in your mobile app. The options available to you depend on company policy and the settings that your administrator has preselected.



## Procedure

1.  Access the settings screen.

    Choose the *Settings* \(![](images/iOS_Icon_Settings_inverted_098f4e8.jpg)\) icon of the app.

2.  To change a setting, select it.

    **Logon**


    <table>
    <tr>
    <th valign="top">

    App Setting


    
    </th>
    <th valign="top">

    Possible Values


    
    </th>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Account*


    
    </td>
    <td valign="top">
    
    Not applicable


    
    </td>
    <td valign="top">
    
    Data required for the server connection. You enter the URL of the server.

    To authenticate, you have the following options depending on the server configuration:

    You use OAuth. For more information, see[Configuring Identity Authentication In Document Management Service](configuring-identity-authentication-in-document-management-service-cf44481.md).

    For more information, see [Installing the iPad or the iPhone App](installing-the-ipad-or-the-iphone-app-ffe75ca.md).


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Passcode*


    
    </td>
    <td valign="top">
    
    -   Off
    -   On


    
    </td>
    <td valign="top">
    
    Changes the passcode lock settings for this app.The following options are available:

    -   Turn Passcode On \(or Off\)
    -   Change Passcode
    -   Require Passcode: Set the interval after which the passcode must be re-entered if the app is suspended \(for example, *Immediately*\).
    -   Erase Data: Set the number of failed logon attempts after which all data stored in the app is deleted.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Fingerprint or Face ID*


    
    </td>
    <td valign="top">
    
    -   Off
    -   On


    
    </td>
    <td valign="top">
    
    Enables you to use your Fingerprint or Face ID to unlock the app.


    
    </td>
    </tr>
    </table>
    
    **General**


    <table>
    <tr>
    <th valign="top">

    App Setting


    
    </th>
    <th valign="top">

    Possible Values


    
    </th>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Cache Size*


    
    </td>
    <td valign="top">
    
    -   No Cache
    -   50 MB
    -   100 MB
    -   1000 MB
    -   5000 MB


    
    </td>
    <td valign="top">
    
    Sets the maximum storage that is used for caching files after download so that they do not need to be downloaded again each time you open them. This setting does not affect files marked for sync.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Show File Extensions*


    
    </td>
    <td valign="top">
    
    -   Off \(default\)
    -   On


    
    </td>
    <td valign="top">
    
    Turns the display of all file extensions in the document lists on or off.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Show Thumbnails*


    
    </td>
    <td valign="top">
    
    -   On \(default\)
    -   Off


    
    </td>
    <td valign="top">
    
    Disables the display of thumbnail images for files \(PDFs, Apple Quicktime videos, or images\) that you have opened or that you keep in sync.


    
    </td>
    </tr>
    </table>
    
    **Synchronization**


    <table>
    <tr>
    <th valign="top">

    App Setting


    
    </th>
    <th valign="top">

    Possible Values


    
    </th>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Automatic Sync Over Cellular*


    
    </td>
    <td valign="top">
    
    -   Off \(default\)
    -   On


    
    </td>
    <td valign="top">
    
    Enables automatic synchronization of files over a cellular network.

    You can also set a limit in MB for data transferred over a cellular network. A warning is then displayed when transferring files above this limit.


    
    </td>
    </tr>
    </table>
    
    **Dialog Warnings**


    <table>
    <tr>
    <th valign="top">

    App Button


    
    </th>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Reset "Don't Ask Me" Warnings*


    
    </td>
    <td valign="top">
    
    Resets all dialogs for which you chose *Do not show this message again* so that they are displayed again.


    
    </td>
    </tr>
    </table>
    
    **Support**


    <table>
    <tr>
    <th valign="top">

    App Setting


    
    </th>
    <th valign="top">

    Possible Values


    
    </th>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Version*


    
    </td>
    <td valign="top">
    
     


    
    </td>
    <td valign="top">
    
    Displays the version of the app, for example, 1.1.0.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Support Log*


    
    </td>
    <td valign="top">
    
    -   Off \(default\)
    -   On


    
    </td>
    <td valign="top">
    
    If you switch the log on, you can define the maximum number of log files \(1, 2, 5, or 10\).


    
    </td>
    </tr>
    </table>
    

**Related Information**  


[Calling Up Help](calling-up-help-0a079a9.md "In the iOS app of Document Management Service, a question mark symbol is displayed. Its context menu contains configurable help entries.")

[Updating and Sorting the Documents List](updating-and-sorting-the-documents-list-69ed225.md "The Document Management Service app refreshes the list of documents whenever you navigate to a folder.")

[Working with Selected Files in the Documents List](working-with-selected-files-in-the-documents-list-809e18a.md "The documents list displays a list of files and subfolders when you access any folder in SAP Document Management Service.")

[Navigating Using Breadcrumbs](navigating-using-breadcrumbs-66bff8e.md "In the SAP Document Management Service iOS client you can switch easily to parent folders of the current folder.")

[Sharing Files](sharing-files-3907e7c.md "You can share files with colleagues and business partners by creating a link to a share containing the files you want to share. You can distribute the link by e-mail, instant messaging, or social networks, wherever you want.")

[Creating a Share](creating-a-share-a7e4209.md "You can create an empty share in Collaboration of the iOS app.")

[Receiving an Invitation to a Share](receiving-an-invitation-to-a-share-23338a4.md "In SAP Document CenterSAP Mobile Documents, share administrators can invite other users to become share members.")

[Synchronizing Files Automatically](synchronizing-files-automatically-c5c68c5.md "The mobile apps of SAP Document CenterSAP Mobile Documents can keep your files up to date on your device, even if you do not access the files. In addition, the files are still available when you are offline and have no network access.")

[Checking the App Connection Status \(iPad\)](checking-the-app-connection-status-ipad-d2e3a48.md "On the iPad, the connection status of the SAP Document Management Service app is displayed for quick reference.")

[Adding and Deleting Files and Folders](adding-and-deleting-files-and-folders-1365ee1.md "In the SAP Document Management Service mobile app, you can add and delete files and folders.")

[Presenting PDF Files on iOS](presenting-pdf-files-on-ios-86a70b5.md "With the iOS apps of SAP Document CenterSAP Mobile Documents, you can present PDF files using an external display.")

[Editing PDF Files on iOS](editing-pdf-files-on-ios-7f9ee7f.md "In the SAP Document CenterSAP Mobile Documents iOS client you can easily annotate PDF files or fill in PDF forms. However, you can only work on editable PDFs and cannot change the text of the PDF itself.")

[Saving Files from Outside SAP Document Management Service](saving-files-from-outside-sap-document-management-service-35bba2b.md "In the SAP Document Management Service mobile app you can save files from other applications.")

[Opening Files from Outside SAP Document Management Service](opening-files-from-outside-sap-document-management-service-229039c.md "On iOS devices, you can access files that are stored in SAP Document Management Service from other applications that support Apple's Document Provider extension.")

[Single Sign-On for iOS App Using X.509 Certificates](single-sign-on-for-ios-app-using-x-509-certificates-e49e4b1.md "You can configure your iPad or iPhone SAP Document CenterSAP Mobile Documents app with a certificate for logging on without a user name and password.")

[Using the Pushed Documents Repository](using-the-pushed-documents-repository-b50785e.md "The Pushed Documents repository of SAP Document CenterSAP Mobile Documents gives an overview of all pushed documents that are automatically downloaded to your device.")

[Searching for Files and Folders](searching-for-files-and-folders-dcab658.md "The SAP Document Management Service mobile app enables you to search offline and online for files and folders in any repository and browse the search results quickly and easily.")

[Using Favorites](using-favorites-8c5a10c.md "To quickly access specific files or folders, you can add links to these items and store them in the Favorites folder.")

[Versioning of Files](versioning-of-files-bf2c605.md)

[Viewing and Editing Properties of Files and Folders](viewing-and-editing-properties-of-files-and-folders-d161100.md "In the SAP Document Management Service mobile app you can view the properties of a file or a folder and edit some of these properties.")

[Starting and Using Executive Mode for iOS](starting-and-using-executive-mode-for-ios-b206afc.md "The executive mode of the SAP Document CenterSAP Mobile Documents iOS app is a clear, minimized user interface for viewing shared content.")

[Using Stored Web Links](using-stored-web-links-0943d86.md "You can open stored Web links on your iOS device.")

