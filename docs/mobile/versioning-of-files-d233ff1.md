<!-- loiod233ff1a75b64efa8cec093e034c90f0 -->

# Versioning of Files

The SAP Document CenterSAP Mobile Documents Web app enables you to create new versions of a file, access previous versions, delete any of the versions stored, and restore a new file to a previous version. Versioning in SAP Document CenterSAP Mobile Documents is also helpful for teamwork, where you are collaborating with colleagues on projects and the content goes through several iterations of improvement and review. This way, you can track the file history and the development of the final version.



## Prerequisites

-   Your administrator has setup repository in SAP Document Center Admin UI for My Documents, Shared Documents and Document Service based corporate repositories.
-   Your administrator has setup your repository as versioned in the CMS back-end system for other repositories.



## Context

If your back-end system is Microsoft SharePoint, the following applies:

-   You can edit only the latest version of the file you want to modify.
-   The comment for the latest version does not appear on the *Document Versions* tab, but it is displayed correctly when a new version is created.



## Procedure

1.  Choose the file for which you want to create a new version by selecting the checkbox next to its file name.

2.  From the actions bar, choose *Check Out* to download the file for editing.

3.  Edit the file offline and then choose *Check In* to upload its new version.

    A popup window for uploading the file, setting the version to major or minor, and commenting appears.

    > ### Note:  
    > If you want to cancel the creation of the new file version, choose *Cancel Checkout*.

4.  Choose *OK*.

5.  To check the new versions of a file, select the file checkbox and then choose the *Properties* icon.

    The *Document Versions* tab shows you the existing file versions, who has modified the file, the date of modification, comments, and the actions allowed.

6.  When you select a particular version of a file, you can *Download* or *Restore* it.

    In order to avoid duplicate versioning, no other user is allowed to edit a file while you are editing it.


