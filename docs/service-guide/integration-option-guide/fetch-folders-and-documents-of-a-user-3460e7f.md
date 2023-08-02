<!-- loio3460e7ff924143018aa9727e9b3249b0 -->

# Fetch Folders and Documents of a User

As a data protection and privacy admin, you can list all the folders and documents created or modified by a given user.





### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/<i class="varname">&lt;parameter1&gt;</i></code>

**HTTP Method:***GET*

**Permissions:** DPP Admin for Document Management Service, Integration Option

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\)



### Request Headers


<table>
<tr>
<th valign="top">

Header



</th>
<th valign="top">

Required



</th>
<th valign="top">

Values



</th>
</tr>
<tr>
<td valign="top">

`x-EcmUserDPP`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

Unique identifier registered in the Identity Provisioning system. Could be an email ID or user name.



</td>
</tr>
</table>



### Request Parameters


<table>
<tr>
<th valign="top">

Parameter



</th>
<th valign="top">

Required



</th>
<th valign="top">

Value



</th>
</tr>
<tr>
<td valign="top">

`parameter1`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

dpp



</td>
</tr>
</table>



### Request Example

```


GET https://<"endpoints" : "ecmservice" : "url">.cfapps.eu10.hana.ondemand.com/rest/v2/dpp



```



### Response Example

```


{
    "gdprReport": {
        "repositories": [],
        "hasMoreItems": false
    }
}


```

