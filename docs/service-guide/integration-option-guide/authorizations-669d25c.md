<!-- loio669d25caffe246178e0c36826427ae51 -->

# Authorizations

The APIs can be accessed by specific users based on their authorizations.

Document Management Service, Integration Option APIs are protected with the following roles:


<table>
<tr>
<th valign="top">

Application



</th>
<th valign="top">

Roles



</th>
</tr>
<tr>
<td valign="top">

Document Management or CMIS APIs



</td>
<td valign="top">

`SDM_User`



</td>
</tr>
<tr>
<td valign="top">

Admin or Repository management APIs



</td>
<td valign="top">

`SDM_Admin`



</td>
</tr>
<tr>
<td valign="top">

Migration APIs



</td>
<td valign="top">

`SDM_MigrationAdmin`



</td>
</tr>
<tr>
<td valign="top">

Retentions and Holds on CMIS objects



</td>
<td valign="top">

`SDM_BusinessAdmin`



</td>
</tr>
</table>

> ### Note:  
> There's no need to add these roles to the technical user flow \(use the client credentials to get a token using a client ID and secret\). By default, these responsibilities have been assigned. These scopes must be added only for the normal user flow.

**Related Information**  


[Personas](../concepts/personas-2b6b3c4.md "You can perform different activities in the Document Management Service based on your roles and authorizations. Knowing who the personas are that use a product is an effective way to understand the needs of your users.")

