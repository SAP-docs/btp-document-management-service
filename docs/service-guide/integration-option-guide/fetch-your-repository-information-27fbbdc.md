<!-- loio27fbbdcf48b644bd8ed1426171c898d7 -->

# Fetch Your Repository Information

Fetch the details of a single repository.





### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories/<i class="varname">&lt;repository_id&gt;</i></code>

**HTTP Method:***GET*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\).



### Request Example

```


GET https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories/repository_id


```



### Response Example

A sample success response for the GET request for a given repository ID.

```


{

	{
		"connection": {
			"destination": "Destination Name",
			"type": "service"
			},

		"repository": {
			"cmisRepositoryId": "CMIS Repository Id given during onboard",
			"createdTime": "Creation TimeStamp",
			"id": "SDM Reposiotry Id",
			"lastUpdatedTime": "LastUpdated TimeStamp",
			"name": "Repository Name",
			"repositoryCategory": "repositoryCategory",
			"repositorySubType": "SAP DMS",
			"repositoryType": "external"
			}

	}	

}


```

