<!-- loio615286deed794ed6a88eb688ce96e169 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Migrating Across Data Centers

Migrate SAP Document Management Service from one data center to another in the Cloud Foundry environment.



<a name="loio615286deed794ed6a88eb688ce96e169__prereq_z5n_c1j_crb"/>

## Prerequisites

You've created HTTP destination and selected the following parameters. For more information, see [Create HTTP Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/783fa1c418a244d0abb5f153e69ca4ce.html).


<table>
<tr>
<th valign="top">

Property

</th>
<th valign="top">

Value

</th>
</tr>
<tr>
<td valign="top">

`URL`

</td>
<td valign="top">

API URL of the source Document Management Service instance in the Cloud Foundry environment.

</td>
</tr>
<tr>
<td valign="top">

`Authentication` 

</td>
<td valign="top">

`OAuth2ClientCredentials`

</td>
</tr>
<tr>
<td valign="top">

`Client ID` 

</td>
<td valign="top">

Enter `clientid` that you've generated and copied from your subaccount.

</td>
</tr>
<tr>
<td valign="top">

`Client Secret`

</td>
<td valign="top">

Enter `clientsecret` that you’ve generated and copied from your subaccount.

</td>
</tr>
<tr>
<td valign="top">

`Token Service URL`

</td>
<td valign="top">

Enter `tokenurl` that you've generated and copied from your subaccount.

</td>
</tr>
</table>



## Context

You can migrate without causing the data loss using *Document Management Service Migration* tool.



## Procedure

1.  Open the *Document Management Migration* view.

2.  Choose :heavy_plus_sign: icon.

3.  In the dialog box that appears, choose *Document Management Service Across Data Centers* option.

4.  Select the *Destination Name* from the drop-down menu.

5.  **Optional:** In the *Target Repository* section, choose the following:

    *Encryption*: Select encryption option if you want to encrypt your data in the target repository.

    *Thumbnail*: Select the thumbnail if you want to enable it in the target repository.

6.  Choose *Migrate*.

    Wait for the migration to complete and once done successfully, you can check the status on migrations screen.


