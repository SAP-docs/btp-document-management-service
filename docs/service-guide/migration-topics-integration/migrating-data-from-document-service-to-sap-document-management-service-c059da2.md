<!-- loioc059da232d2340fb850dc62395ad14a0 -->

# Migrating Data from Document Service to SAP Document Management Service

This topic describes the steps you need to take when migrating the data from Document Service in Neo environment to SAP Document Management Service in the Cloud Foundry environment without causing the data loss using API.



<a name="loioc059da232d2340fb850dc62395ad14a0__prereq_jdv_chw_znb"/>

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
    
    Instance URL of the Documentation Service in the Neo environment
    
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
    
    Email ID of the user with the `manageECM` scope
    
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
    



## Context

> ### Remember:  
> -   You must run the API for any delta changes.
> 
> -   Moving an object to another folder won't be reflected because the move action isn't supported.
> -   For old objects, ACL changes won't be reflected.

To assist you, we've created a precheck that includes everything you need to make sure your data is ready to migrate from Document Service to SAP Document Management Service.

The general process of migrating data is as follows:

<a name="task_z2q_kgg_ppb"/>

<!-- task\_z2q\_kgg\_ppb -->

## Run a Precheck

Use this API to carry out a precheck before you migrate.



<a name="task_z2q_kgg_ppb__context_uw2_mgg_ppb"/>

## Context

Before you start the migration, you can run a precheck API to make sure all of the migration requirements are met and all issues are resolved. The system performs a set of prechecks before an actual migration is executed.

After you've completed the prechecks, you can check the status and proceed as required.



### Request

**URI:** <code><i class="varname">&lt;"endpoints":"migrationservice":"url"&gt;</i>/v1/precheck</code>

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

`accountId`

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Technical name of your subaccount in the Neo environment.

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

Unique name of the repository that you want to migrate.

</td>
</tr>
<tr>
<td valign="top">

`repoKey`

</td>
<td valign="top">

Yes

</td>
<td valign="top">

The key value of the repository.

</td>
</tr>
<tr>
<td valign="top">

`destination`

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Name of the destination that you created in the Cloud Foundry environment.

</td>
</tr>
<tr>
<td valign="top">

`userMapping`

</td>
<td valign="top">

Optional

</td>
<td valign="top">

A user-mapping file that compares the user identifier used in the Document Service to the user identifier that you choose to use in Document Management.

> ### Note:  
> The mapping is only needed if the user ID is different from the identity provider used in Neo and Cloud Foundry environment.

For example, if user identifier is the user ID in Neo environment and email ID in the Cloud Foundry, then you provide a json file with following format.

> ### Sample Code:  
> ```
> {"UserID 1":"Email ID 1","UserID 2":"Email ID 2"}
> 
> ```



</td>
</tr>
</table>



### Request Example

```
POST  https:<"endpoints":"migrationservice":"url">/v1/precheck
```



### Response Sample

A sample success response for the *POST* request that returns the following message.

```
Check migration status at /status/accountId/repoId
```

<a name="task_ucp_xhg_ppb"/>

<!-- task\_ucp\_xhg\_ppb -->

## Perform Migration

Use this instruction to migrate data from Document Service in Neo environment to SAP Document Management Service in the Cloud Foundry environment.



<a name="task_ucp_xhg_ppb__context_ghw_yhg_ppb"/>

## Context

With minimal disruption, you can migrate existing Neo to the Cloud Foundry environment using this API.



### Request

**URI:** <code><i class="varname">&lt;"endpoints":"migrationservice":"url"&gt;</i>/v1/migrate</code>

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

`accountId`

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Technical name of your subaccount in the Neo environment.

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

Unique name of the repository that you want to migrate.

</td>
</tr>
<tr>
<td valign="top">

`repoKey`

</td>
<td valign="top">

Yes

</td>
<td valign="top">

The key value of the repository.

</td>
</tr>
<tr>
<td valign="top">

`destination`

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Name of the destination that you created in the Cloud Foundry environment.

</td>
</tr>
<tr>
<td valign="top">

`userMapping`

</td>
<td valign="top">

Optional

</td>
<td valign="top">

A user-mapping file that compares the user identifier used in the Document Service to the user identifier that you choose to use in Document Management.

> ### Note:  
> The mapping is only needed if the user ID is different from the identity provider used in Neo and Cloud Foundry environment.

For example, if user identifier is the user ID in Neo environment and email ID in the Cloud Foundry, then you provide a json file with following format.

> ### Sample Code:  
> ```
> {"UserID 1":"Email ID 1","UserID 2":"Email ID 2"}
> 
> ```



</td>
</tr>
</table>



### Request Example

```
POST  https:<"endpoints":"migrationservice":"url">/v1/migrate

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

A sample success response for the *GET* request that returns the status and the percentage of the migration.

```

[
{
"tenant": "6xx8d6xx-bxx3-xxdx-axfx-xxx3x4x0018xx",
"replicated": 0,
"total": 905675300,
"percent": 100,
"inProgress": true,
"triggerDate": "2021-01-19T11:09:07.5315109Z"
}
]

```

