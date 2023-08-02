<!-- loiodb20ee0e90dd4546845de19cf3c758dc -->

# Access Your Repository

Access the repository after the admin connects it with Document Management Service, Integration Option.





### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/browser</code>

**HTTP Method:***GET*

**Permissions:** User of Document Management Service, Integration Option via the scope `SDM_User`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\).



### Request Example

```


GET https://<"endpoints" : "ecmservice" : "url">/browser


```



### Response Example

```


{
    CMIS repository information
}


```

