<!-- loio2860a1fdf3cf4541b2c8f7db4003c8a4 -->

# Count and List All Repositories

As an admin, you can count and list all the repositories connected to Document Management Service, Integration Option.



<a name="loio2860a1fdf3cf4541b2c8f7db4003c8a4__section_kjj_vlb_wcb"/>

## Count All Onboarded Repositories



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories/count</code>

**HTTP Method:***GET*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\)



### Request Example

```


GET https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories/count



```



### Response Example

A sample success response for the GET request that returns the count of all the repositories that you added.

```


  {
   "count": 1
  }


```



<a name="loio2860a1fdf3cf4541b2c8f7db4003c8a4__section_xys_4kv_5lb"/>

## List All Onboarded Repositories



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories</code>

**HTTP Method:***GET*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\)



### Request Example

```


GET https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories



```



### Response Example

A sample success response for the GET request that includes all of the repositories that you added.

```


{

"repoAndConnectionInfos": 
[
	{
		... //Multiple Repository Information
	},

	{
		"connection": {
			"destination": "Destination Name",
			"type": "service"
		},

		"repository": {
			"cmisRepositoryId": "CMIS Repository Id given during onboard",
			"createdTime": "Creation TimeStamp",
			"id": "Document Management Repository Id"
,
			"lastUpdatedTime": "LastUpdated TimeStamp",
			"name": "Repository Name",
			"repositoryCategory": "repositoryCategory",
			"repositorySubType": "SAP DMS",
			"repositoryType": "external"
		}
	}
]
}


```

The *id* parameter returns the Document Management Service, Integration Option generated identifier for your repository. You can use the value to fetch the properties of the repository, update, and delete the repository.

