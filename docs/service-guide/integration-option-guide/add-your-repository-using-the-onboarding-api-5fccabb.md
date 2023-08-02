<!-- loio5fccabb78c564bcf95f209909b66c4de -->

# Add Your Repository Using the Onboarding API

Add your repository to Document Management Service, Integration Option.





### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories</code>

**HTTP Method:***POST*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\).



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

`"repository":"displayName"`



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

`"repository":"description"`



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

`"repository":"repositoryType"`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

`external`

The value "external" means that you're adding your own repository. To use SAP provided repository, see [Connecting to Document Management Service, Repository Option Using API](connecting-to-document-management-service-repository-option-using-api-d30200e.md).



</td>
</tr>
<tr>
<td valign="top">

`"repository":"repositoryId"`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

CMIS ID of your repository



</td>
</tr>
<tr>
<td valign="top">

`"repository":"repositoryParams":"paramName"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

`contentServer`

The parameter is needed only for SAP DMS repositories to bypass ABAP layer and directly communicate to the content server to upload documents.



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

Content-server destination name

The parameter is needed only for SAP DMS repositories to bypass ABAP layer and directly communicate to the content server to upload documents.



</td>
</tr>
<tr>
<td valign="top">

`"repository":"externalId"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Unique name for the repository

The parameter is mandatory only for the users of SAP S/4HANA who use Document Management Service, Integration Option for their SAP S/4HANA Attachment service.



</td>
</tr>
<tr>
<td valign="top">

`"connection":"displayName"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Display name for the destination



</td>
</tr>
<tr>
<td valign="top">

`"connection":"description"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Description for the destination



</td>
</tr>
<tr>
<td valign="top">

`"connection":"destinationName"`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

Name of the destination that you configured in the [prerequisites](https://help.sap.com/viewer/f6e70dd4bffa4b65965b43feed4c9429/Cloud/en-US/21bd2788d7c74c43a399dc13cf452f0c.html).



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
	"repositoryType": "external",
	"repositoryId": "CMIS repository ID",
	"externalId": "Unique name for the repository",
	"repositoryParams":[ {
            "paramName" :"contentServer",
            "paramValue": "<CONTENT_SERVER_DESTINATION_NAME>"
        } ]
  },
    "connection": {
    "destinationName": "Name of the destination"
  }
}


```



### Response Example

```


{
    "<id>": "Onboarded SDM Repository ID",

		//Details of the created repository are returned

}


```

