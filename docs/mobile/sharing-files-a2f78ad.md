<!-- loioa2f78adfe03f43c89bc861f240e30c2d -->

# Sharing Files

You can share files with colleagues and business partners by creating a link to a share containing the files you want to share. You can distribute the link by e-mail, instant messaging, or social networks, wherever you want.



<a name="loioa2f78adfe03f43c89bc861f240e30c2d__prereq_N10015_N10012_N10001"/>

## Prerequisites

-   Your administrator has set up a *Shared Documents* repository.
-   Your administrator has set up a combination of confidentiality levels and security policies that allow files to be shared.



## Context

You create a share that contains the files you want to share, and decide who should have access to this share. You can limit access to the share to named users \(members\) and assign them permissions using roles. Then, you can send a link by e-mail to these members. In addition, you can let anonymous users access the share by sending a public link, and even assign write permission so that they can change, upload, and delete files. The share is then public and anyone with the link can access it, even if they have not installed SAP Document CenterSAP Mobile Documents.

The public link is available only for shares and cannot link directly to subfolders or files of the share. You can create the share first and add the public link later on. For more information, see [Adding a Link to a Share](https://help.sap.com/viewer/ba2adb991f6e4b6a857e9f76a99402bd/Cloud/en-US/99bb4a32a8024e8fad90e92f46040831.html "In SAP Document Center, you can create shares without a link that anyone can access.") :arrow_upper_right:.

> ### Note:  
> Note that if your company uses a user quota to limit the amount of data each user is allowed to store in SAP Document CenterSAP Mobile Documents, the data on the share is assigned to the quota of the share owner. Even if other users upload documents to the share, the quota of the share owner is used.



## Procedure

1.  In the folder containing the files you want to share, select the files to share from the documents list and choose *Share*.

    -   If you want to copy your files, choose *Copy to Share*.

    -   If you want to move your files, choose *Move to Share*.

    A list of the existing shares to which you are assigned as owner, administrator, or contributor is displayed, as well as the *Create Share* button. If you choose a share from the list and choose *OK*, your file is copied or moved to the selected share. You can either close the dialog using *OK*, send an e-mail containing the share link, or copy the share link \(if the respective links have been added to the share\).

2.  Create a new share by choosing *Create Share*. Enter a name for the share.Replace the suggested name *New Share* with a more meaningful name for the share.

    > ### Note:  
    > Be aware that this name is visible to the people you send the link to.

3.  Define the access settings of your share using the following options:


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
    
    *Access expiration date* 


    
    </td>
    <td valign="top">
    
    Defines when the access to the share expires. If the expiration period times outand you have not defined a date for automatic deletion, the share will not be removed. You as the share owner or a share administrator can access and extend this period.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Delete share permanently after expiration* 


    
    </td>
    <td valign="top">
    
    To delete the share permanently after the public link has expired, select *Delete share permanently after expiration*. Then select the period of grace before deletion from the dropdown list.

    > ### Caution:  
    > The share will be deleted permanently and cannot be recovered.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Write permission* 


    
    </td>
    <td valign="top">
    
    Enables users to upload files to the share. If you grant write permission, you can in addition select to hide uploaded files from external users by selecting *Hide uploaded files*. This is to ensure that external users can only see the share but no uploaded files. 


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Password protection* 


    
    </td>
    <td valign="top">
    
    Lets you set a password for accessing the link to the share. The administrator configures whether you need to specify a password and which criteria it must meet, for example, a minimum length.


    
    </td>
    </tr>
    </table>
    
    > ### Tip:  
    > As the share owner or share administrator you can change the settings of the share. To do so directly after creating the share or anytime the share is open, choose the *i Share Details* button. To change these settings from the list of shares, proceed as follows:
    > 
    > 1.  Select your share in the *Shared Documents* folder.
    > 2.  Choose the *Access Settings of Share* icon \(![](images/Web_Icon_Group_77198e9.png)\).
    > 3.  Edit the share settings.
    > 4.  Choose *Save*.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Share with members


    
    </td>
    <td valign="top">
    
    Creates a share that can be accessed only by users with authentication in SAP Document CenterSAP Mobile Documents.

    > ### Tip:  
    > -   To add share members, enter the logon ID or the mail address of the user you want to add.To add share members, either add groups that are available in the SAP BTP cockpit or enter the logon ID or the mail address of the user you want to add. If a user has registered multiple times using the same mail address but different user IDs, select the user based on the user ID that is along with the mail address.
    > -   Specify the member's role as *Administrator*, *Reader*, or *Contributor*. When adding a group to the share, the role can only be specified for the whole group and not for specific members.
    > -   The members are displayed in a list with subsections for administrators, contributors, and readers. If a newly added member has never before logged on to SAP Document CenterSAP Mobile Documents, the name is displayed with the status *Awaiting user's initial logon*.
    > -   To copy the mail addresses of the share members, for example, to use them in the *To* field of a mail containing the share link, choose the *E-Mail Addresses* button. In the box that opens, you can then select and copy the addresses.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Anyone with the link has access

    and

    Share with members


    
    </td>
    <td valign="top">
    
    Creates a public share and anyone with the link can access it, as well as users with authentication in SAP Document CenterSAP Mobile Documents.

    > ### Tip:  
    > You can use all settings that are available for both of the options described above.


    
    </td>
    </tr>
    </table>
    
4.  Optional: To enter a description, choose the *General Properties* \(![](images/Web_Icon_General_Properties_554df7d.png)\) button and insert the text in the *Description* field.

5.  Choose *Save*.

6.  Optional: On the confirmation screen, you can decide to send an e-mail with the link to the share or copy the link URL.

    Alternatively, you can simply choose *OK* to close the dialog. Later on, you will still be able to locate your share in the *Shared Documents* repository and send a link or open the URL from there using the *Access Settings of Share* icon \(![](images/Web_Icon_Group_77198e9.png)\).

    > ### Note:  
    > Do not send the password together with the URL; use another way of sharing it.




## Results

Your new share is displayed in the *Shared Documents* repository.

The recipients of the public link can access the attached files using the link in the e-mail. This link takes the recipients to the public sharing UI, where they can download the attached files. If they are named users of SAP Document CenterSAP Mobile Documents and are members of this share, they can log on to the Web app using the *Member Logon* button and access the attached file in the share instead.

