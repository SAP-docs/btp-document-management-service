<!-- loio926d32b7cd5145acb93c4317f58e2751 -->

# Collaboration Repositories

Learn about the features of collaboration repositories.





### What is a Collaboration Repository?

A collaboration repository offers the capability to create shared folders \(sap:share\) which can be used for collaboration. As an admin, you can create collaboration repositories by passing additional parameter called `"repositoryCategory" : "Collaboration"` in the onboarding API. In collaboration repositories, a user \(share owner\) can create folders of type sap:share that can be used to collaborate by inviting other users \(share members\) and managing access rights.



### Collaboration Repository Capabilities

-   All members of the collaboration repository can create shared folders and normal folders.

-   Users can create share folders \(sap:share\), normal folders \(cmis: folder\) and documents \(cmis:document\) inside a collaboration repository.

-   Users can create a shared folder only in the root folder. It'sn’t possible to create folders of type sap:share inside normal folders or other shared folders.

-   Folders of type cmis:folder and documents created inside a shared folder behave and operate in the same way as it was in normal repositories.




### Shared Folder Capabilities

-   User who creates the shared folder \(sap:share\) is the default owner of that folder.

-   Owner of the shared folder can add members to collaborate.

-   Owner of the shared folder can manage the access rights for the members.

-   Folders of type cmis:folder and documents inside a shared folder inherits the access right of the parent shared folder.

-   Owner of the shared folder can delete the share and its contents.




### Access Control Lists

-   Reuse UI and Document Management Service, Application Option supports ACLs consisting of ACEs \(Access Control Entries\) to control the access to documents and folders as described in the CMIS standard. For the shared folders, Document Management Service supports the following permissions. Share owners can provide access to members with below permission using API to change ACL.


    <table>
    <tr>
    <th valign="top">

    Role
    
    </th>
    <th valign="top">

    Permission
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Reader
    
    </td>
    <td valign="top">
    
    *cmis:read*
    
    </td>
    <td valign="top">
    
    Read the documents.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Contributor
    
    </td>
    <td valign="top">
    
    *sap:delete*
    
    </td>
    <td valign="top">
    
    Create, update, and delete documents and folders.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Administrator
    
    </td>
    <td valign="top">
    
    *cmis:all*
    
    </td>
    <td valign="top">
    
    Delete the share, add users, and manage access rights.
    
    </td>
    </tr>
    </table>
    

