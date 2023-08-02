<!-- loio01fb63bce6354c8d94ce27effae4341d -->

# Access Control Lists

Document Management Service supports Access Control Lists \(ACLs\) consisting of Access Control Entries \(ACEs\) to control the access to documents and folders as described in the CMIS standard.

ACL view is available in the *Properties* view of each document and folder. ACL view shows all the ACLs present in the underlying CMIS repository.

The following ACLs are supported by Document Management Service:

-   `Reader (cmis:read)`
    -   Allows fetching an object \(folder or document\).
    -   Allows reading the ACL, properties, and the content of an object.

-   `Creator (sap:file)`
    -   Includes all privileges of `Reader`.
    -   Allows the creation of objects in a folder and to move an object.

-   `Editor (cmis:write)`
    -   Includes all privileges of `Creator`.
    -   Allows modifying the properties and the content of an object.
    -   Allows checking out of a versionable document.

-   `Contributor (sap:delete)`
    -   Includes all privileges of `Editor`.
    -   Allows the deletion of an object.
    -   Allows checking in and canceling check out of a private working copy.

-   `Administrator (cmis:all)`
    -   Includes all privileges of `Editor`.
    -   Allows modifying the ACL of an object.

-   `Guest {sap:builtin}anonymous`
    -   Includes all privileges of `Reader`.

    -   Guest privileges can be controlled by an administrator.
    -   In the public share, the Guest user has reader access by default.


For a repository, the initial settings for the root folder are:

-   The ACL contains one ACE for the `{sap:builtin}everyone` principal with the `Administrator` permission. With these settings, all principals have full control over the root folder.

-   Without specific ACL settings, all documents and folders possess an ACL with one ACE for the built-in principal `{sap:builtin}everyone` with the `Administrator` permission that grants all users unrestricted access.


