<!-- loio7f59ed09665c4bfbb604bb17437916da -->

# Update Your Repository

Update few parameters of an already onboarded repository. This way you can avoid creating multiple repositories for the same purpose.



<a name="loio7f59ed09665c4bfbb604bb17437916da__section_k3f_dqb_2nb"/>

## Update Your External Repository



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories/<i class="varname">&lt;repository_id&gt;</i></code>

**HTTP Method:***PUT*

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

`"repository":"description"`

</td>
<td valign="top">

Optional

</td>
<td valign="top">

New description for the repository

</td>
</tr>
<tr>
<td valign="top">

`"repository":"repositoryParams":"paramValue"`

</td>
<td valign="top">

Optional

</td>
<td valign="top">

New value for the content server destination

</td>
</tr>
</table>



### Request Example

```


PUT https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories/799b3b26-xxxx-xxxx-xxxx-c5febfd93ca0

{
"repository": {
	"description": "newdescription",
	"repositoryParams": [
	{
	"paramName": "contentServer",
	"paramValue": "NEW_CONTENT_SERVER_DESTINATION_NAME"
	}
	]
	}
}


```



### Response Example

A sample success response for the PUT request that returns the updated parameters for your repository.

```


{
...
"id": "799b3b26-xxxx-xxxx-xxxx-c5febfd93ca0",
"name": "Name of the repository",
"description": "Updated Description",

"repositoryParams": [
{
"paramName": "contentServer",
"paramValue": "NEW_CONTENT_SERVER_DESTINATION_NAME"
}

... //Updated Repository Information
}


```



<a name="loio7f59ed09665c4bfbb604bb17437916da__section_kjj_vlb_wcb"/>

## Update Document Management Service, Repository Option



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories/<i class="varname">&lt;repository_id&gt;</i></code>

**HTTP Method:***PUT*

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

`"description"`

</td>
<td valign="top">

Optional

</td>
<td valign="top">

New description for the repository

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

New value for virus scan

Acceptable values:

-   true – virus scan is enabled and you can upload files only up to 400 MB

-   false \(default value\) – virus scan not performed and you can upload files of any size




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

New value

Applicable only if `"isVirusScanEnabled"` is set to true.

Acceptable values:

-   true – virus scan not performed for uploading files larger than 400 MB. Files smaller than 400 MB are scanned before upload.

-   false \(default value\) – virus scan is enabled and you can upload files only up to 400 MB




</td>
</tr>
</table>



### Request Example

```


PUT https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories/799b3b26-xxxx-xxxx-xxxx-c5febfd93ca0

{
  "repository": {
		"description": "Updated description for the repository",
		"isVirusScanEnabled":"true",
		"skipVirusScanForLargeFile": "true"
  }
}


```



### Response Example

A sample success response for the PUT request that returns the updated parameters for your repository.

```


{
...
"id": "799b3b26-xxxx-xxxx-xxxx-c5febfd93ca0",
"name": "Name of the repository",
"description": "New Updated Description",
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
"paramValue": true
}
],
"repositorySubType": "SAP Document Management",
"repositoryType": "internal"

... //Updated Repository Information
}


```

