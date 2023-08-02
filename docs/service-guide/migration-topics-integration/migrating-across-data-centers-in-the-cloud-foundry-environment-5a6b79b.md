<!-- loio5a6b79b51d6644aea6cb59a784e32fe3 -->

# Migrating Across Data Centers in the Cloud Foundry Environment

This topic describes the steps you need to take when migrating SAP Document Management Service from one data center to another in the Cloud Foundry environment. You can migrate without causing the data loss using REST APIs.



<a name="loio5a6b79b51d6644aea6cb59a784e32fe3__prereq_jdv_chw_znb"/>

## Prerequisites

-   You've subscribed to the service Document Management Service, Integration Option and created an instance in Cloud Foundry environment. See [Initial Setup for Document Management Service, Integration Option](../integration-option-guide/initial-setup-for-document-management-service-integration-option-bc0f1ec.md).

-   The instance must be connected to your application or you've generated the service key.

-   The global administrator of your SAP BTP account has added the service plan for Document Management Service, Repository Option to your subaccount via entitlements. See [Configure Entitlements for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).

-   You've copied the `clientid`, `clientsecret`, and `tokenurl` parameters generated in the same subaccount of Cloud Foundry Environment where Document Management, integration option instance is created. For more information about creating parameters, see [Create Service Keys Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cdf4f200db3e4c248fa67401937b2f78.html).

-   You've generated the bearer token from the client credentials in theSAP Document Management Service. See [Generate a JSON Web Token](../integration-option-guide/generate-a-json-web-token-bff9fd6.md).

-   You've the `SDM_MigrationAdmin` scope to execute the API.

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
    
    API URL of the source Document Management Service instance in the Cloud Foundry environment


    
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
    



<a name="loio5a6b79b51d6644aea6cb59a784e32fe3__context_zrq_mpj_gqb"/>

## Context

> ### Remember:  
> The migration is only relevant to internal repositories, not external repositories.

<a name="task_ucp_xhg_ppb"/>

<!-- task\_ucp\_xhg\_ppb -->

## Perform Migration

Use this instruction to migrate SAP Document Management Service instance from one data center to another in the Cloud Foundry environment.



<a name="task_ucp_xhg_ppb__context_ghw_yhg_ppb"/>

## Context

With minimal disruption, you can execute the following request to initiate the migration:



### Request

**URI:** <code><i class="varname">&lt;"endpoints":"migrationservice":"url"&gt;</i>/v1/migrate/sdm</code>

**HTTP Method:** *POST*

**Permissions:** Administrator or developer role for Document Management, integration option via the scope `SDM_MigrationAdmin`.

**Authentication:** Bearer JSON Web Token.



### Request Parameters


<table>
<tr>
<th valign="top">

Parameter



</th>
<th valign="top">

Mandatory



</th>
<th valign="top">

Value/Description



</th>
</tr>
<tr>
<td valign="top">

`destination`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

Name of the destination that you created.

> ### Example:  
> `ds_cf`



</td>
</tr>
</table>



### Request Example

```
POST  https:<"endpoints":"migrationservice":"url">/v1/migrate/sdm

```



### Response Sample

A sample success response for the *POST* request that returns the following message.

```
Check migration status at /status
```

<a name="task_kdv_ynw_znb"/>

<!-- task\_kdv\_ynw\_znb -->

## Checking the Status of Migration

This section describes the steps you need to check the status of migration.



<a name="task_kdv_ynw_znb__context_vyc_f4w_znb"/>

## Context

The migration status is a *GET* response that can be obtained by executing the following request.



### Request

**URI:** <code><i class="varname">&lt;"endpoints":"migrationservice":"url"&gt;</i>/v1/status/</code>

**HTTP Method:** *GET*

**Permissions:** Administrator or developer role for Document Management, integration option via the scope `SDM_MigrationAdmin`.

**Authentication:** Bearer JSON Web Token.



### Request Example

```
GET  https:<"endpoints":"migrationservice":"url">/v1/status/
```



### Response Sample

A sample success response for the *GET* request that returns the status and the progress report of the migration.

> ### Sample Code:  
> ```
> 
> "sdm-di-dev":{​​​​​​​​
> "d39abcd9-0811-4cca-81d0-52be03253ebe":[
> {​​​​​​​​
> "tenant":"2ac****1-ed0f-41a7-8a80-ca1b577f8bb8",
> "targetRepoID":"c87****0-06d8-4af7-97fb-1cd51ca92d14",
> "replicatedSize":612572158,
> "totalSize":612572158,
> "percentSize":100,
> "replicatedObjectCount":18,
> "totalObjectCount":18,
> "inProgress":false,
> "triggerDate":"2021-06-30T06:19:28.9296307Z",
> "repositoryType":"SDM",
> "status":"COMPLETED"
> }​​​​​​​​,
> {​​​​​​​​
> "tenant":"201****b-869e-4c89-acf3-a419fbc28095",
> "targetRepoID":"79eabcd4-49e7-4739-bd79-76e6a7e3a6eb",
> "replicatedSize":1222462,
> "totalSize":1222462,
> "percentSize":100,
> "replicatedObjectCount":8,
> "totalObjectCount":8,
> "inProgress":false,
> "triggerDate":"2021-06-30T06:20:08.558338Z",
> "repositoryType":"SDM",
> "status":"COMPLETED"
> }​​​​​​​​,
> {​​​​​​​​
> "tenant":"7eabc5fe-749f-4277-a60f-275da1090b7c",
> "targetRepoID":"761abcd4-394e-43dc-92c8-ecfb3c24080b",
> "replicatedSize":0,
> "totalSize":0,
> "percentSize":0,
> "replicatedObjectCount":0,
> "totalObjectCount":0,
> "inProgress":false,
> "triggerDate":"2021-06-30T06:20:15.5835197Z",
> "repositoryType":"SDM",
> "status":"COMPLETED"
> }​​​​​​​​
> ]
> }​​​​​​​​
> 
> 
> ```

