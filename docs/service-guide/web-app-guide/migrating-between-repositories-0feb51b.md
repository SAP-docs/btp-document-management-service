<!-- loio0feb51b9355e41369d1b13d078dd10cb -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Migrating Between Repositories

Migrate between repositories of SAP Document Management Service in the Cloud Foundry environment.



<a name="loio0feb51b9355e41369d1b13d078dd10cb__prereq_tjq_3xq_2tb"/>

## Prerequisites

-   You've created HTTP destination and selected the following parameters. For more information, see [Create HTTP Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/783fa1c418a244d0abb5f153e69ca4ce.html).


    <table>
    <tr>
    <th valign="top">

    Property


    
    </th>
    <th valign="top">

    Value


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    `URL`


    
    </td>
    <td valign="top">
    
    The repository's CMIS browser binding URL.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `User` 


    
    </td>
    <td valign="top">
    
    The repository's username.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Password` 


    
    </td>
    <td valign="top">
    
    For the given username, a password is required.


    
    </td>
    </tr>
    </table>
    
-   You’ve copied the Repository ID and Object ID from the web link of a particular folder or file in the source and target repositories.



<a name="loio0feb51b9355e41369d1b13d078dd10cb__context_zd4_4xq_2tb"/>

## Context

In the migration tool, you can use migration between repositories option, which allows you to copy or move from one repository \(consisting of files, folders, or a combination of both\) to another. It also supports copying a single document. This feature is useful for organizations that need to transfer large amounts of data quickly and securely.



## Procedure

1.  Navigate to the *Document Management Migration* view.

2.  Choose :heavy_plus_sign: icon.

3.  In the dialog box that appears, choose *Between Repositories* option.

4.  Choose *Destination Name* from the drop-down.

5.  In the *Source Repository* section, enter the following details:

    1.  Enter source *Repository ID*. It's the unique ID of the repository that you want to migrate from the source repository.

    2.  Enter source *Object ID*. It's the ID of the source object of the folder or document that you want to migrate.


    > ### Note:  
    > You can copy the *Repository ID* and *Object ID* from the web link of the particular folder or file.

6.  In the *Target Repository* section, enter the following details:

    1.  Enter target *Repository ID*. It's the unique ID of the repository that you want to migrate to the target repository.

    2.  Enter target *Object ID*. It's the ID of the target object of the folder or document.


7.  Choose *Migrate*.

    Wait for the migration to complete. Depending on the size of the repository, migration can take some time. You can see the current status by refreshing the table.


