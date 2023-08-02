<!-- loio2f448be6acf147b4ac3dc2fa0cd5341d -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Migrating to SAP Document Management Service 

This topic describes the steps that you need to follow when migrating from SAP Document Center and Document Service in the Neo environment to SAP Document Management Service. You can also migrate across data centers in SAP Document Management Service.



<a name="loio2f448be6acf147b4ac3dc2fa0cd5341d__prereq_x13_xqp_j4b"/>

## Prerequisites

-   You've the migration admin role assigned to your user profile via scope `SDM_MigrationAdmin` and `SDMWeb_Migration`.

-   You've created HTTP destination and entered the following parameters. Create separate destination based on the application that you want to migrate. For more information, see [Create HTTP Destinations](https://help.sap.com/viewer/DRAFT/cca91383641e40ffbe03bdc78f00f681/Validation/en-US/783fa1c418a244d0abb5f153e69ca4ce.html).


    <table>
    <tr>
    <th valign="top">

    SAP Document Center


    
    </th>
    <th valign="top">

    Document Service


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    

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
    
    Tenant URL of the SAP Document Center in the Neo environment


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Authentication`


    
    </td>
    <td valign="top">
    
    `BasicAuthentication`


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `User`


    
    </td>
    <td valign="top">
    
    Email ID of the admin user


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Password`


    
    </td>
    <td valign="top">
    
    Password


    
    </td>
    </tr>
    </table>
    

    
    </td>
    <td valign="top">
    

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
    
    Tenant URL of the Documentation Service in the Neo environment

    > ### Example:  
    > Go to the Neo subaccount where you created the document service repository. Copy the landscape's URL from your browser. `https://ecm.eu2.hana.ondemand.com`


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Authentication`


    
    </td>
    <td valign="top">
    
    `BasicAuthentication`


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `User`


    
    </td>
    <td valign="top">
    
    Email ID of the admin user with the `manageECM` scope


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Password`


    
    </td>
    <td valign="top">
    
    Password


    
    </td>
    </tr>
    </table>
    

    
    </td>
    </tr>
    </table>
    



## Context

An application migration addresses the steps needed to migrate the application and its data to a normal business processes with minimal disruptions. You can migrate across data centers for SAP Document Management Service. And also from third-party CMIS repositories to SAP Document Management Service.



## Procedure

1.  Open the *Document Management Migration* view.

2.  Choose :heavy_plus_sign: icon at the top-right corner of the page.

3.  In the dialog box that appears, choose one of the following applications:

    -   SAP Document Center

    -   Document Service

    -   Document Management Service Across Data Centers. For more information, see [Migrating Across Data Centers](migrating-across-data-centers-615286d.md).

    -   Third-Party Repository. For more information, see [Migrating from Third-Party CMIS Repository](migrating-from-third-party-cmis-repository-a02649a.md).

    -   Between Repositories. For more information, see [Migrating Between Repositories](migrating-between-repositories-0feb51b.md).


4.  If you’re migrating from SAP Document Center, choose *SAP Document Center* and enter the following details:


    <table>
    <tr>
    <th valign="top">

    Field


    
    </th>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    `Destination Name`


    
    </td>
    <td valign="top">
    
    Name of the destination that you created in the Cloud Foundry environment.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Under *Source Repository* section, `Account ID`


    
    </td>
    <td valign="top">
    
    Technical name of your subaccount.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Repository ID`


    
    </td>
    <td valign="top">
    
    Unique ID of the repository that you want to migrate.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `User Mapping`


    
    </td>
    <td valign="top">
    
    A user-mapping file that compares the user identifier used in the Document Center to the user identifier that you choose to use in Document Management.

    > ### Note:  
    > The mapping is only needed if the user ID is different from the identity provider used in Neo and Cloud Foundry environment.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    

    <table>
    <tr>
    <th valign="top">

    Target Repository


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Encryption


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Thumbnail


    
    </td>
    </tr>
    </table>
    

    
    </td>
    <td valign="top">
    

    <table>
    <tr>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Select encryption option if you want to encrypt your data in the target repository.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Select the *Thumbnail* if you want to enable it in the target repository.


    
    </td>
    </tr>
    </table>
    

    
    </td>
    </tr>
    </table>
    
5.  If you’re migrating from Document Service, choose *Document Service* and enter the following details:


    <table>
    <tr>
    <th valign="top">

    Field


    
    </th>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    `Destination Name`


    
    </td>
    <td valign="top">
    
    Name of the destination that you created in the Cloud Foundry environment.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Under *Source Repository* section,`Account ID`


    
    </td>
    <td valign="top">
    
    Technical name of your subaccount.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Repository ID`


    
    </td>
    <td valign="top">
    
    Unique name of the repository that you want to migrate.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Repository Key`


    
    </td>
    <td valign="top">
    
    The key value of the repository.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `User Mapping`


    
    </td>
    <td valign="top">
    
    A user-mapping file that compares the user identifier used in the Document Service to the user identifier that you choose to use in Document Management.

    > ### Note:  
    > The mapping is only needed if the user ID is different from the identity provider used in Neo and Cloud Foundry environment.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Select Tenants`


    
    </td>
    <td valign="top">
    
    It's an array of tenants mentioned in the JSON file format that you would like to migrate.

    > ### Note:  
    > This option is only available in the delta migrations.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    

    <table>
    <tr>
    <th valign="top">

    Target Repository


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Encryption


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Thumbnail


    
    </td>
    </tr>
    </table>
    

    
    </td>
    <td valign="top">
    

    <table>
    <tr>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Select encryption option if you want to encrypt the data in the target repository.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Select the *Thumbnail* if you want to enable it in the target repository.


    
    </td>
    </tr>
    </table>
    

    
    </td>
    </tr>
    </table>
    
6.  Choose *Migrate*. Wait for the migration to complete and once done successfully, you can check the status on migrations.

    > ### Tip:  
    > Download logs for migration with a noncompleted status and check for detailed information.


Delta Migration

A delta migration only update the repository details that have been modified since the previous migration.

7.  Select one of the completed migrations.

8.  Choose <span class="SAP-icons"></span> Migrate Again option.

9.  Enter the details again if you want to modify.

10. Choose *Migrate*.


**Related Information**  


[Migrating Across Data Centers](migrating-across-data-centers-615286d.md "Migrate SAP Document Management Service from one data center to another in the Cloud Foundry environment.")

[Migrating from Third-Party CMIS Repository](migrating-from-third-party-cmis-repository-a02649a.md "Migrate third-party CMIS repositories to SAP Document Management Service in the Cloud Foundry environment.")

