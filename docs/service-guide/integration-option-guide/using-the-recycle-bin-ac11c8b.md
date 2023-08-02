<!-- loioac11c8b243e7402990023be2c7335861 -->

# Using the Recycle Bin

Use recycle bin to restore your documents and folders.

Recycle bins are repository-specific. It's supported only for Document Management Service, Repository Option. A recycle bin contains only the files and folders that were deleted in a specific repository. In addition, you can also permanently delete selected files and folders or all content from a repository recycle bin. If you don't restore the objects, they'll be permanently delete automatically after a period of 14 days by default.

The following rules apply to the deleted files and folders:

-   You can't update a deleted file or create a new version for it unless you restore it first.
-   Files and folders in the recycle bin must be restored before you can edit or download them.
-   You can only restore a complete folder with all its content, not parts of it.
-   If file name conflicts occur, the restore operation fails with a name constraint violation. You've to ensure manually that no file with the same name exists in the original location.
-   You find restored files and folders in their former location, that is, the repository that you deleted them from.
-   The content of the recycle bin isn't added to your user quota, but is automatically deleted after a specified period of time.
-   As a default, the retention period is 14 days. If you want to restore, you need to do it within the retention period, otherwise the documents and folders are permanently deleted .

**Related Information**  


[Deleting and Restoring Files and Folders](deleting-and-restoring-files-and-folders-af6b72b.md "You can delete files and folders from the Document Management Service repositories.")

