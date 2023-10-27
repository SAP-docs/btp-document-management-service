<!-- loio0c5ea974ee3a4135a5dd47dc08c2cc1c -->

# Migrating from SAP Document Center to SAP Document Management Service

This topic describes the steps you need to take when migrating the SAP Document Center for Neo environment to SAP Document Management Service in the Cloud Foundry environment without causing the data loss using APIs.



<a name="loio0c5ea974ee3a4135a5dd47dc08c2cc1c__prereq_jdv_chw_znb"/>

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
    
    Tenant URL of the Document Center in the Neo environment
    
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
    



## Context

With minimal disruption, you can migrate SAP Document Center existing in the Neo to the Cloud Foundry environment using API. There are no additional configurations required from your end.



### Request

**URI:** <code><i class="varname">&lt;"endpoints":"migrationservice":"url"&gt;</i>/v1/migrate/sdc</code>

**HTTP Method:** *POST*

**Permissions:** Administrator or developer role for Document Management Service, Integration Option via the scope `SDM_MigrationAdmin`.

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

Unique ID of the repository that you want to migrate.

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

Name of the destination that you've created in the Cloud Foundry environment.

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

A user-mapping file that compares the user identifier used in the SAP Document Center to the user identifier that you choose to use in Document Management service.

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
POST  https:<"endpoints":"migrationservice":"url">/v1/migrate/sdc
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

**Permissions:** Administrator or developer role for Document Management Service, Integration Option via the scope `SDM_MigrationAdmin`.

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

<a name="task_wvd_l1d_t4b"/>

<!-- task\_wvd\_l1d\_t4b -->

## Migrate Cloud Content Bridge \(CCB\) Repository

This section describes the steps that you need to follow if you want to migrate CCB repository using REST-based API.



<a name="task_wvd_l1d_t4b__context_ewm_y1d_t4b"/>

## Context

You can migrate your CCB repository to the SAP Document Management Service by executing the following request.



### Request

**URI:** <code><i class="varname">&lt;"endpoints":"migrationservice":"url"&gt;</i>/v1/migrate/ccb</code>

**HTTP Method:** *POST*

**Permissions:** The `Administrator` and `Content Bridge Support` role has to be in the Neo sub account of the user whose credentials are provided at the destination.

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

Unique ID of the repository that you want to migrate.

</td>
</tr>
<tr>
<td valign="top">

`s4account`

</td>
<td valign="top">

Yes

</td>
<td valign="top">

S4 tenant account connected to your Cloud Foundry environment.

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

Name of the destination that you've created in the Cloud Foundry environment.

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

A user-mapping file that compares the user identifier used in the SAP Document Center to the user identifier that you choose to use in Document Management service.

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
POST  https:<"endpoints":"migrationservice":"url">/v1/migrate/ccb
```



### Response Sample

A sample success response for the *POST* request that returns the following message.

> ### Example:  
> Check migration status at /status

