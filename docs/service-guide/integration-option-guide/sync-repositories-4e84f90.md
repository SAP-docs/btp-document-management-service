<!-- loio4e84f90269b44daab3701d7fe4e7a91b -->

# Sync Repositories

As an admin, you can sync the metadata of the repositories with Document Management Service, Integration Option.



<a name="loio4e84f90269b44daab3701d7fe4e7a91b__section_kjj_vlb_wcb"/>

## Sync All Repositories



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories/sync</code>

**HTTP Method:***GET*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\)



### Request Example

```


GET https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories/sync



```



### Response Example

```


  {
   "message": "Sync successful"
  }


```



<a name="loio4e84f90269b44daab3701d7fe4e7a91b__section_mx3_pmr_4mb"/>

## Sync Individual Repository



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories/sync/<i class="varname">&lt;repositoryID&gt;</i></code>

**HTTP Method:***GET*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\)



### Request Example

```


GET https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories/sync/479f6857-ab54-86086a3394db



```

To fetch a repository ID, see [Count and List All Repositories](count-and-list-all-repositories-2860a1f.md).



### Response Example

```


  {
   "message": "Sync successful"
  }


```

