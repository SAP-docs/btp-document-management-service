<!-- loio6758fd98b8a643cf85d0026bf82f792d -->

# Using the Recycle Bin

Your administrator can activate a recycle bin for a repository, for example, the *My Documents* or *Shared Documents* repositories.



Recycle bins are repository-specific. Your administrator can activate bins for one or more repositories. A recycle bin contains only the files and folders that were deleted in a specific repository. If you do not restore the objects, they will be cleaned up automatically after a period of time defined by your administrator. In addition, you can also permanently delete selected files and folders or all content from a repository recycle bin.

The following rules apply to deleted files and folders:

-   You cannot update a deleted file or create a new version for it unless you restore it first.
-   Files and folders in the recycle bin must be restored before you can edit or download them.
-   You can only restore a complete folder with all its content, not parts of it.
-   If file name conflicts occur, the restore operation fails with a name constraint violation. You have to ensure manually that no file with the same name exists in the original location. Folders with the same name will be merged if they do not contain files or folders with the same name.
-   You find restored files and folders in their former location, that is, the repository that you deleted them from.
-   The content of the recycle bin is not added to your user quota, but is automatically deleted after a specified period of time.

The recycle bin contains entries for the following repository types:

-   *My Documents*

    Deleted files and folders can only be accessed by their owner. You can restore files and folders until the recycle bin is automatically cleaned up, for example, for a 30-day period.

-   *Shared Documents*

    Deleted shares, files, and folders can only be restored by their owner. If a share is deleted, it loses all its properties. Even if you restore it, it remains a plain share without members or public link settings. The share owner has to add the members again. If a share administrator deletes a share, it is moved to the owner's recycle bin. Only the owner can then restore the share. If you restore files, not shares, the restored files inherit the current access right settings of the share.

-   *Corporate Documents*

    Only users who are configured as administrators for a repository can restore or permanently delete objects from the recycle bin. All access rights are inherited from the original parent folder. Original ACLs \(if specific to the deleted object\) are not preserved. If you restore a folder of a repository with a local repository connection, you have to create a new list of users who have permission to access the folder. See Managing Folders in Document Service Repositories in the cloud admin guide.

-   *Favorites*

    Deleted files and folders can only be accessed by their owner. You can restore files and folders until the recycle bin is automatically cleaned up, for example, for a 30-day period.


**Related Information**  


[Deleting and Restoring Files and Folders](https://help.sap.com/viewer/ba2adb991f6e4b6a857e9f76a99402bd/Cloud/en-US/da94f79fd379411fbe5b698c380e7110.html "You can delete files and folders from the My Documents, Shared Documents, and Corporate Documents repositories.") :arrow_upper_right:

