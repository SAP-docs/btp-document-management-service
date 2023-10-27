<!-- loio1ceb1c8f64da4efe9a19a690c424fad0 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Create a Shared Folder and Define Its Access

As a member of a collaboration-enabled repository, create a shared folder and configure who can access the folder also public share via the link.



<a name="loio1ceb1c8f64da4efe9a19a690c424fad0__prereq_gkq_djh_qmb"/>

## Prerequisites

You’re part of a collaboration-enabled Document Management repository. See [Onboarding Internal Repository](../web-app-guide/onboarding-internal-repository-59e3cb7.md).



## Procedure

1.  Open a collaboration-enabled repository.

2.  Choose *Create* \> *Share*.

3.  Enter a name for your shared folder and choose *Save*.

4.  Choose the <span class="SAP-icons"></span> More Options for the folder that you created and then *Edit*.

5.  Choose the *Share Settings* tab and define the access settings for your share using the following options:


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
    
    *Anyone with link has access*
    
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
    
    Defines when the access to the share expires. If the expiration period times out, you as the share owner or share administrator can access and extend this period.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Write permission*
    
    </td>
    <td valign="top">
    
    Enables users to upload files to the share. If you grant write permission, in addition you can select to hide uploaded files from external users by selecting *Hide uploaded files*. It's ensure that external users can only see the share but no uploaded files.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Hide uploaded files*
    
    </td>
    <td valign="top">
    
    Select to hide uploaded files from external users by selecting *Hide uploaded files*. It's ensure that external users can only see the share but no uploaded files.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Password protection*
    
    </td>
    <td valign="top">
    
    Lets you set a password for accessing the link to the share. The administrator configures whether you need to specify a password and which criteria it must meet, for example, a minimum length.

    > ### Note:  
    > If an incorrect password is entered, the share is locked for 30 seconds after 3 unsuccessful attempts.


    
    </td>
    </tr>
    </table>
    
    > ### Note:  
    > If you enable this option, a *Guest* user with reader permission is added to the shared member's list by default. The *Guest* user can access all the shared documents, but they can't edit or delete them. Later, the administrator can control the *Guest* user permissions. It's possible for a *Guest* user to be a contributor as well if the admin checks the *Write Permission* option and sets the contributor access. The administrator can also remove the guest user from the shared member's list at any time by unchecking the *Anyone with link has access* option. It would make the public share a member share.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Share with members*
    
    </td>
    <td valign="top">
    
    Creates a share that can be accessed only by users with authentication in SAP Document Management Service.

    > ### Tip:  
    > -   To add share members, either enter the user ID of the members separated by commas or enter the logon ID or the mail address of the user you want to add. If a user has registered multiple times using the same mail address but different user IDs, select the user based on the user ID that is along with the mail address.
    > 
    > -   Specify the member's role as *Reader*, *Contributor, or* *Administrator*. The members are displayed in a list with their respective role.
    > 
    >     -   *Reader*: A permission granting a specific user the read-only access. A Reader can only view the folder and its contents.
    > 
    >     -   *Contributor*: A Contributor can add, edit, and delete content.
    >     -   *Administrator*: An administrator can navigate to the shared folder and have a control on it. You can restrict access to the respective files, add new members, and also manage user roles.


    
    </td>
    </tr>
    </table>
    
    By default, you’re already added as the Administrator for the shared folder.

6.  Enter the user ID of the user with whom you want to collaborate. Choose *Add*.

    > ### Note:  
    > The user ID depends on the attributes you configure with Platform Identity Provider service or your own Identity Provider.

7.  In the *All Users* list, pick a role for the user.

8.  Choose *Save*. You can later edit the folder properties to remove the users.


