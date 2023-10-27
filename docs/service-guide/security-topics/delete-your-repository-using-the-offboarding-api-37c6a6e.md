<!-- loio37c6a6eec3c149589eb6cd1bd13f229c -->

# Delete Your Repository Using the Offboarding API

Delete your repository from Document Management Service, Integration Option.



<a name="loio37c6a6eec3c149589eb6cd1bd13f229c__section_kjj_vlb_wcb"/>

## Delete a Repository



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories/<i class="varname">&lt;id&gt;</i></code>

**HTTP Method:***DELETE*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](../integration-option-guide/generate-a-json-web-token-bff9fd6.md)\).



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

`id`

</td>
<td valign="top">

Yes

</td>
<td valign="top">

ID that Document Management Service generated when you added the repository. See [API Documentation](https://help.sap.com/viewer/disclaimer-for-links?q=https://api.sap.com/package/SAPDocumentManagementServiceIntegrationOption?section=Artifacts).

</td>
</tr>
</table>



### Request Example

```


DELETE https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories/f651ed69-****-****-****-d372441131fe


```



### Response Example

A sample success response for the DELETE request:

```



{
"message": "Repository with id:f651ed69-****-****-****-d372441131fe deleted"
}


```



<a name="loio37c6a6eec3c149589eb6cd1bd13f229c__section_bmd_nmj_hlb"/>

## Delete Multiple Repositories

If you have multiple repositories, you can delete all of them in one go. You can do so by removing the `id` in the request URI.

```


DELETE https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories


```



### Response Example

A sample success response for the DELETE request:

```


{
"message": "All Repositories associated with instance have been deleted"
}


```

