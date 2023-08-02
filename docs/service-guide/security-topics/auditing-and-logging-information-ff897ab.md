<!-- loioff897abf23024eb6a38bff071b8482c2 -->

# Auditing and Logging Information

Here you can find a list of the security events that are logged by Document Management Service, Integration Option and Document Management Service, Application Option.

**Security events written in audit logs**


<table>
<tr>
<th valign="top">

Event grouping



</th>
<th valign="top">

What events are logged



</th>
<th valign="top">

How to identify related log events



</th>
<th valign="top">

Additional information



</th>
</tr>
<tr>
<td valign="top" rowspan="9">

Configuration Changes



</td>
<td valign="top">

Create repository



</td>
<td valign="top">

**Create event:** Onboard repository with repository onboarding API or via admin UI.



</td>
<td valign="top" rowspan="9">

Following roles need to be assigned in your subaccount:

-   auditlog-viewer!

-   auditlog-management!




</td>
</tr>
<tr>
<td valign="top">

Update repository



</td>
<td valign="top">

**Update event:** Update repository with repository onboarding API or via admin UI.



</td>
</tr>
<tr>
<td valign="top">

Delete repository



</td>
<td valign="top">

**Delete event:** Delete repository with repository onboarding API or via admin UI.



</td>
</tr>
<tr>
<td valign="top">

Create configurations



</td>
<td valign="top">

**Create event:** Create repository with repository onboarding API or via admin UI.



</td>
</tr>
<tr>
<td valign="top">

Update configurations



</td>
<td valign="top">

**Update event:** Update repository with repository onboarding API or via admin UI.



</td>
</tr>
<tr>
<td valign="top">

Delete configurations



</td>
<td valign="top">

**Delete event:** Delete repository with repository onboarding API or via admin UI.



</td>
</tr>
<tr>
<td valign="top">

Create cloud connection



</td>
<td valign="top">

**Create event:** Create repository with repository onboarding API or via admin UI.



</td>
</tr>
<tr>
<td valign="top">

Update cloud connection



</td>
<td valign="top">

**Update event:** Update repository with repository onboarding API or via admin UI.



</td>
</tr>
<tr>
<td valign="top">

Delete cloud connection



</td>
<td valign="top">

**Delete event:** Delete repository with repository onboarding API or via admin UI.



</td>
</tr>
<tr>
<td valign="top" rowspan="4">

Document changes



</td>
<td valign="top">

Create documents



</td>
<td valign="top">

**Create event:** Create document using UI action or CMIS create document API.



</td>
<td valign="top" rowspan="4">

 



</td>
</tr>
<tr>
<td valign="top">

Read documents



</td>
<td valign="top">

**Read event:** When user download or open file from UI or via CMIS `getContentStream` API.



</td>
</tr>
<tr>
<td valign="top">

Delete documents



</td>
<td valign="top">

**Delete event:** Delete document using UI action or CMIS delete document API.



</td>
</tr>
<tr>
<td valign="top">

Modify ACL



</td>
<td valign="top">

**Create event:** Modify ACL by calling applyACL methods or from UI action.



</td>
</tr>
</table>

**Related Information**  


[Audit Logging in the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/f92c86ab11f6474ea5579d839051c334.html)

[Audit Logging in the Neo Environment](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/02c39712c1064c96b37c1ea5bc9420dc.html)

