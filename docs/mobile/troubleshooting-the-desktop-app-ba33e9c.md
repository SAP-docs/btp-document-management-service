<!-- loioba33e9c0071a45e590ceaa25ff8bd149 -->

# Troubleshooting the Desktop App

Consider the following when troubleshooting errors that occur in your desktop app.



<a name="loioba33e9c0071a45e590ceaa25ff8bd149__section_overlay_icons"/>

## Sync Status Overlay Icons Not Visible

The overlay icons display the current sync status for a file or a folder. If you don't see these overlay icons, this can be because of the following reasons:

-   The SAP Document Management Service app is not running. You can verify this by looking at the tray icon for SAP Document Management Service. If it is not running, start the SAP Document Management Service app.

-   Other applications are already consuming 15 overlay icons, which is the limit set by Microsoft Windows. Windows Explorer can load up to 15 overlay icons, and the operating system reserves four icons for its own use. To find out how many overlay icons you have registered, check the registry:

    1.  Press the Windows key + R, and then enter `regedit`.

    2.  Navigate to the `ShellIconOverlayIdentifiers` registry key at: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\ShellIconOverlayIdentifiers`

    3.  If the SAP Document Management Service overlay icons are among the first 15 icons listed, they will be displayed. Otherwise, you'll need to move them up the list.

        > ### Note:  
        > To do this, you must delete or reprioritize other applications' overlay icons. Only proceed if you are absolutely sure what to do.

    4.  If you decide to proceed, select individual keys and delete them by right-clicking the desired key and choosing *Delete* from the context menu. If you don’t want to delete them, rename them. Start the name with a "Z" to send them to the end of the alphabetically sorted list.

    5.  Close Windows Explorer, and then start `explorer.exe` from the Task Manager, or restart your computer.

    6.  Start SAP Document Management Service. The sync icons should re-appear.





<a name="loioba33e9c0071a45e590ceaa25ff8bd149__section_external_device"/>

## Warning Messages When Copying Files to an External Device

If you copy files from your SAP Document Management Service folder to an external device, you might get a warning popup from Microsoft Windows telling you that properties will not be copied.

The SAP Document Management ServiceSAP Document Management Service desktop app stores some technical information in files as custom properties. On file systems like FAT32, which do not support custom properties when you copy such files, a warning message appears.



<a name="loioba33e9c0071a45e590ceaa25ff8bd149__section_fat32"/>

## Desktop App Does Not Sync Files to FAT32-Based Storage

The SAP Document Management Service desktop app stores some technical information in files as custom properties. Therefore, the file system must support custom properties. Because FAT32 does not support custom properties, files might not be properly synced.



<a name="loioba33e9c0071a45e590ceaa25ff8bd149__section_renaming_subfolder"/>

## Renaming a Subfolder Containing Another Subfolder Does Not Work on Microsoft Windows Desktop App

**Symptom**

You have created a folder with a subfolder and another sub-subfolder. If you try to rename the first subfolder or the folder, you get an error message ***Folder In Use***.

**Solution**

To rename the subfolder, use any of the other SAP Document Management Service apps, for example, the Web app.



<a name="loioba33e9c0071a45e590ceaa25ff8bd149__section_qgj_db5_vz"/>

## On Microsoft Windows: Context Menu Action *SAP Document Mangement Service* Doesn’t Appear

**Symptom**

You want to use one of the actions from the SAP Document Management Service context menu, for example, *Rename Share*,*Edit Share*. But when you right click the relevant location, the action doesn’t appear.

**Solution**

If the full path to the document or folder exceeds 255 characters, the context menu *SAP Document Management Service* does not appear. You can execute these actions from the Web app or reduce the length of path.

