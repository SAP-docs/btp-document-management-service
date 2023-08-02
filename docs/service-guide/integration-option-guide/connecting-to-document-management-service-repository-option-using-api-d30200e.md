<!-- loiod30200e0993a457888db2786d4bb5cd9 -->

# Connecting to Document Management Service, Repository Option Using API

Connect your instance of Document Management Service, Integration Option to Document Management Service, Repository Option for file storage.



<a name="loiod30200e0993a457888db2786d4bb5cd9__section_omg_5kd_rlb"/>

## Prerequisites

-   Add the entitlements for Document Management Service, Repository Option to the same subaccount where Document Management Service, Integration Option instance is created. See [Configure Entitlements for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).

-   You've completed one of these tasks for Document Management Service, Integration Option:

    -   [Bind Service Instances to Applications Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/2d2a3e8b2f1348ffbb54eaae10d80b95.html)

    -   [Create Service Keys Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cdf4f200db3e4c248fa67401937b2f78.html).


-   [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)

-   You've the `SDM_Admin` scope to execute the admin APIs.




The API for onboarding repositories can be found in our SAP Business Accelerator Hub. For more information, see [SAP Business Accelerator Hub](https://api.sap.com/api/AdminAPI/resource).





### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories</code>

**HTTP Method:***POST*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JSON Web Token



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

Values/Description



</th>
</tr>
<tr>
<td valign="top">

`"displayName"`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

Name of the repository that appears in the application



</td>
</tr>
<tr>
<td valign="top">

`"description"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Description of the repository



</td>
</tr>
<tr>
<td valign="top">

`"repositoryType"`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

`internal` 



</td>
</tr>
<tr>
<td valign="top">

`"repositoryCategory"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

`Collaboration`

This entry is needed only when you want to create shared folders in the repository. By default, shared folder creation is disabled. For more information, see [Collaboration Repositories](collaboration-repositories-926d32b.md).



</td>
</tr>
<tr>
<td valign="top">

`"isVersionEnabled"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

To maintain multiple versions of your documents

Acceptable values: true/false

Default value: false



</td>
</tr>
<tr>
<td valign="top">

`"isVirusScanEnabled"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

To scan the documents before you upload them

Acceptable values:

-   true – enable virus scan and you can upload files only up to 400 MB

-   false \(default value\) – no virus scan and you can upload files of any size




</td>
</tr>
<tr>
<td valign="top">

`"skipVirusScanForLargeFile"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Applicable only if `"isVirusScanEnabled"` is set to true.

Acceptable values:

-   true – no virus scan for uploading files larger than 400 MB

-   false \(default value\) – can't upload files larger than 400 MB




</td>
</tr>
<tr>
<td valign="top">

`"hashAlgorithms"`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

Hashing algorithms to generate a content hash for all your documents. Acceptable values:

-   `MD5`

-   `SHA-1`

-   `SHA-256`

-   `None` \(default value\) – choose this option if you don't want to generate content hash.




</td>
</tr>
<tr>
<td valign="top">

`"externalId"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Unique name for the repository.

The parameter is mandatory only for SAP S/4HANA attachment service scenarios.



</td>
</tr>
<tr>
<td valign="top">

`"isContentBridgeEnabled"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Acceptable values: true/false

The parameter is mandatory only for SAP S/4HANA attachment service scenarios.



</td>
</tr>
<tr>
<td valign="top">

`"isThumbnailEnabled"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Acceptable values: `true` or `false`.



</td>
</tr>
</table>



### Request Example

```


POST https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories

{
  "repository": {
		"displayName": "Name of the repository",
		"description": "Description for the repository",
		"repositoryType": "internal",
		"isVersionEnabled":"true",
		"isVirusScanEnabled":"true",
		"skipVirusScanForLargeFile": "false",
		"hashAlgorithms":"SHA-256"
  }
}


```



### Response Example

```


{

"id": "1ab2ec0a-db7b-xxxx-xxxx-440fd8ccc85e", //generated Reposiotry ID
"name": "Name of the repository",
"description": "Description for the repository",
"repositoryParams": [
{
"paramName": "isVersionEnabled",
"paramValue": true
},
{
"paramName": "isVirusScanEnabled",
"paramValue": true
},
{
"paramName": "hashAlgorithms",
"paramValue": "SHA-256"
},
{
"paramName": "skipVirusScanForLargeFile",
"paramValue": false
}
],
"repositorySubType": "SAP Document Management",
"repositoryType": "internal"

}


```

