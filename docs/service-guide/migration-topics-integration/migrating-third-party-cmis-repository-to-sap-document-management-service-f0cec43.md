<!-- loiof0cec43862644ac48046e1379f2062f6 -->

# Migrating Third-Party CMIS Repository to SAP Document Management Service

This topic describes the steps you need to take when migrating third-party CMIS repositories to SAP Document Management Service in the Cloud Foundry environment. You can migrate without causing the data loss using REST APIs.



<a name="loiof0cec43862644ac48046e1379f2062f6__prereq_jdv_chw_znb"/>

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
    

<a name="task_ucp_xhg_ppb"/>

<!-- task\_ucp\_xhg\_ppb -->

## Perform Migration

Use the following instruction to migrate third-party CMIS repositories.



<a name="task_ucp_xhg_ppb__context_ghw_yhg_ppb"/>

## Context

With minimal disruption, you can execute the following request to initiate the migration:



### Request

**URI:** <code><i class="varname">&lt;"endpoints":"migrationservice":"url"&gt;</i>/v1/migrate/cmis</code>

**HTTP Method:** *POST*

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
<tr>
<td valign="top">

`repoId`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

ID of the repository.



</td>
</tr>
<tr>
<td valign="top">

`name`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

Enter any name for the repository to make it easier to find later.



</td>
</tr>
<tr>
<td valign="top">

`versionable`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

True or false



</td>
</tr>
<tr>
<td valign="top">

`virusScan`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

True or false



</td>
</tr>
</table>



### Request Example

```
POST  https:<"endpoints":"migrationservice":"url">/v1/migrate/cmis

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
> "fileshare": {
>  "test": [
>  {
>  "tenant": "test",
>  "targetRepoID": "f67416fc-0d2a-43a8-a284-af5bab6bf601",
>  "replicatedSize": 107119078,
>  "totalSize": 4402087957,
>  "percentSize": 2.4333696,
>  "replicatedObjectCount": 26,
>  "totalObjectCount": 30,
>  "inProgress": false,
>  "triggerDate": "2021-08-27T09:01:53.1110247Z",
>  "repositoryType": "SDM",
>  "status": "COMPLETED"
>  }
>  ]
>  }
> 
> 
> 
> ```

