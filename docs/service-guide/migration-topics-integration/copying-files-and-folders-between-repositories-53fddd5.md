<!-- loio53fddd50607e4b8aa14bf24b6c527eb6 -->

# Copying Files and Folders Between Repositories

You can copy your files and folders between repositories in SAP Document Management Service on the SAP BTP, Cloud Foundry environment.



<a name="loio53fddd50607e4b8aa14bf24b6c527eb6__prereq_s1g_sdy_rbc"/>

## Prerequisites

-   You've subscribed to the service Document Management Service, Integration Option and created an instance in SAP BTP, Cloud Foundry environment. See [Initial Setup for Document Management Service, Integration Option](../integration-option-guide/initial-setup-for-document-management-service-integration-option-bc0f1ec.md).

-   The global administrator of your SAP BTP account has added the service plan for Document Management Service, Repository Option to your subaccount via entitlements. See [Configure Entitlements for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).

-   You've copied the `clientid`, `clientsecret`, and `tokenurl` parameters generated in the same subaccount of SAP BTP, Cloud Foundry environment where Document Management Service, Integration Option instance is created. For more information about creating parameters, see [Create Service Keys Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cdf4f200db3e4c248fa67401937b2f78.html).

-   You've copied the `objectId` of the target folder.

-   you've copied the following parameters from both the source and target instances.

    -   `sourceRepositoryId`
    -   `targetRepositoryId`
    -   `targetParentFolderId`

-   You've got the `SDM_MigrationAdmin` scope to run the API.

-   You've created an HTTP destination in both source and target instances, and have updated the following parameters. For more information, see [Create HTTP Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/783fa1c418a244d0abb5f153e69ca4ce.html).


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
    
    API URL of the source Document Management Service, Integration Option instance in the SAP BTP, Cloud Foundry environment.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Authentication` 
    
    </td>
    <td valign="top">
    
    `OAuth2ClientCredentials`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Client ID` 
    
    </td>
    <td valign="top">
    
    Enter `clientid` that you've generated and copied from your subaccount.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Client Secret`
    
    </td>
    <td valign="top">
    
    Enter `clientsecret` that you’ve generated and copied from your subaccount.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `Token Service URL`
    
    </td>
    <td valign="top">
    
    Enter `tokenurl` that you've generated and copied from your subaccount.
    
    </td>
    </tr>
    </table>
    



## Context

As an administrator, you can copy files and folders from one repository to another in the SAP Document Management Service on SAP BTP, Cloud Foundry environment. By leveraging the `Copy API` that is published on the SAP Business Accelerator Hub, you can accomplish this task ensuring a safe and secure transfer of your data.



## Procedure

1.  Access the [Copy API](https://api.sap.com/api/MigrationAPI/resource/Copying_a_file_or_folder_between_repositories) available on the SAP Business Accelerator Hub.

2.  Log on to the SAP Business Accelerator Hub and select the *Try Out* option.

3.  In the body section, provide all the necessary details to leverage the copy functionality.


