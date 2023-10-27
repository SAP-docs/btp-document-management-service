<!-- loio90faa8c52bbc40119bf41def24c3ac94 -->

# Create a Repository Using the Onboarding API for Google Drive

Create your repository to Document Management Service, Integration Option as it's required for establishing a connection with Google Drive.





### Prerequisites:

-   You've generated a JSON Web Token \(JWT\) that serves as your authorization for making API calls. For more information, see [Generating the JSON Web Token \(JWT\)](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md#loio90faa8c52bbc40119bf41def24c3ac94__section_thx_jk2_jvb).

-   You've copied the *URI* value from the service key of Document Management Service, Integration Option. For more information, see [Creating a Service Instance and Service Key](integration-option-guide/creating-a-service-instance-and-service-key-fe7f1e5.md).






### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories</code>

**HTTP Method:***POST*

**Permissions:** Admin for Document Management Service, Integration Option via the `SDM_Admin` scope

**Authentication:** Bearer JWT \(token from [Generating the JSON Web Token \(JWT\)](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md#loio90faa8c52bbc40119bf41def24c3ac94__section_thx_jk2_jvb)\).



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

Name of the repository that appears in the application.

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

Description of the repository.

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

It means that you're adding your own repository.

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

Get the repository ID of a folder, My Drive, or a Shared Drive. For more information about finding IDs, see [Find the Repository IDs](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md#loio90faa8c52bbc40119bf41def24c3ac94__section_udl_5b1_3vb).

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

Unique name for the repository.

The parameter is mandatory for SAP S/4HANA users who use Document Management Service, Integration Option for their SAP S/4HANA Attachment service.

</td>
</tr>
<tr>
<td valign="top">

`"repository":"repositoryCategory"`

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Enter `GoogleWorkspace`.

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

Name of the destination that you configured in the [Prerequisites](https://help.sap.com/viewer/f6e70dd4bffa4b65965b43feed4c9429/Cloud/en-US/21bd2788d7c74c43a399dc13cf452f0c.html).

</td>
</tr>
</table>



### Request Example

<code>POST https://<i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/repositories</code>

```

{
"repository": {
"displayName": "<Name of the repository>",
"description": "<Description for the repository>",
"repositoryType": "external",
"externalId": "<Unique name for the repository>",
"repositoryCategory": "GoogleWorkspace",
"repositoryId": "<ID of the folder to be considered as root folder>"
},
"connection": {
"destinationName": "<Drive destination>"
}
}
```



<a name="loio90faa8c52bbc40119bf41def24c3ac94__section_thx_jk2_jvb"/>

## Generating the JSON Web Token \(JWT\)

Use the parameters from the service key of Document Management Service, Integration Option instance to generate a JSON Web Token \(JWT\).



### Request

**HTTP Method:***POST*

**Authentication:** Basic.

**User name**: *<"uaa" : "clientId"\>*

**Password**: *<"uaa" : "clientSecret"\>*

**URI:**<code><i class="varname">&lt;"uaa" : "url"&gt;</i>/oauth/token?grant_type=client_credentials&amp;authorities=&lt;AUTHORITIES&gt;</code>. For *<AUTHORITIES\>*, encode the following values:

`{"az_attr":{"X-EcmUserEnc":"<Your BTP user ID>","X-EcmAddPrincipals":"<Your name>"}}` 

> ### Sample Code:  
> ```
> <"uaa" : "url">/oauth/token?grant_type=client_credentials&authorities=%7B%22az_attr%22%3A%7B%22X-EcmUserEnc%22%3A%22abc%40xyz.com%22%2C%22X-EcmAddPrincipals%22%3A%22abc%22%7D%7D
> 
> ```

**Response:** In the response, you see the access token \(JWT\) that you need to make the onboarding API requests.

> ### Note:  
> By default you're using a `client_credentials` grant type token. If you don't pass *<authorities\>* for generating JSON Web Token, then you need to pass the `"X-EcmUserEnc": "<emailId>"` header in any API request to the Document Management Service, Integration Option API.



<a name="loio90faa8c52bbc40119bf41def24c3ac94__section_udl_5b1_3vb"/>

## Find the Repository IDs

You can find detailed instructions on how to obtain the repository IDs of My Drive, Shared Drives, and folders in this section.


<table>
<tr>
<th valign="top">

Google Drive Folders

</th>
<th valign="top">

Repository ID

</th>
</tr>
<tr>
<td valign="top">

Root of Google Drive

</td>
<td valign="top">

`GoogleConnectorEntry`

</td>
</tr>
<tr>
<td valign="top">

Shared with me

</td>
<td valign="top">

`SharedWithMe`

</td>
</tr>
<tr>
<td valign="top">

Shared drives

</td>
<td valign="top">

`SharedDrives`

</td>
</tr>
<tr>
<td valign="top">

Any shared drive within Shared Drives folder

</td>
<td valign="top">

See [Steps to Find the ID of a Shared Drive or a Folder](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md#loio90faa8c52bbc40119bf41def24c3ac94__section_a1z_fjd_jvb)

</td>
</tr>
<tr>
<td valign="top">

Any folder

</td>
<td valign="top">

See [Steps to Find the ID of a Shared Drive or a Folder](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md#loio90faa8c52bbc40119bf41def24c3ac94__section_a1z_fjd_jvb)

</td>
</tr>
<tr>
<td valign="top">

My Drive

</td>
<td valign="top">

See [Steps to Find the ID of My Drive](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md#loio90faa8c52bbc40119bf41def24c3ac94__section_glr_ljd_jvb)

</td>
</tr>
</table>



<a name="loio90faa8c52bbc40119bf41def24c3ac94__section_a1z_fjd_jvb"/>

## Steps to Find the ID of a Shared Drive or a Folder

1.  Open Google Drive using any web browser.

2.  Select a Shared Drive or a folder.

3.  Upon clicking, the URL of the selected item changes in the browser.

4.  The ID of the selected item appears in the last string of the URL.

    > ### Example:  
    > When you click on a folder or shared drive, you get the following URL in your browser: `https://drive.google.com/drive/u/2/folders/QWERTYUIOP12345`. In this case, [QWERTYUIOP12345\] is the ID for the selected item that can be set with `repositoryId` parameter and becomes the root of the onboarded repository.




<a name="loio90faa8c52bbc40119bf41def24c3ac94__section_glr_ljd_jvb"/>

## Steps to Find the ID of My Drive

1.  Navigate to the portal [Google Drive API Files: get](https://developers.google.com/drive/api/v3/reference/files/get).

2.  Enter `root` for value of the `fileId` parameter in *Try this method* section on the right.

3.  Click *Execute*.

4.  There may be a pop-up prompting you to sign into your Google account. Sign in with your Google Workspace account.

5.  You'll see the response after the request has been executed. My drive's ID is the value of the *id* property in the response.

    > ### Example:  
    > ```
    > 
    > {
    >   "kind": "drive#file",
    >   "id": "0AGew2YmLjh20Uj8RSD",
    >   "name": "My Drive",
    >   "mimeType": "application/vnd.google-apps.folder"
    > }
    > 
    > ```


**Related Information**  


[Setting Up a Google Workspace Account](setting-up-a-google-workspace-account-9670f69.md "Create your Google Workspace Account to connect to Document Management Service, Integration Option.")

[Creating HTTP Destinations](creating-http-destinations-2b04ac7.md "Create destinations in your SAP BTP subaccount to connect Google Drive with Document Management Service, Integration Option.")

[Managing Cross-Domain Mapping](managing-cross-domain-mapping-96d2d97.md "Manage cross-domain mapping if your domain is different from the Google Workspace domain.")

[Supporting CMIS APIs](supporting-cmis-apis-4288da6.md "Following is a list of all supported CMIS (Content Management Interoperability Services) REST APIs.")

[Establishing Trust Configuration Between SAP S/4HANA Cloud And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-cloud-and-sap-btp-66f91a9.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA Cloud, import the SAML identity provider metadata to the Cloud Foundry account.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA Cloud And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-cloud-and-sap-btp-26f9c07.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA Cloud and SAP BTP.")

[Maintain Business Roles Within the SAP S/4HANA Cloud](maintain-business-roles-within-the-sap-s-4hana-cloud-091973b.md "Create and maintain business roles based on the selected business catalogs.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-on-premise-and-sap-btp-699a106.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA (on premise) and SAP BTP.")

[Maintain Business Roles Within SAP S/4HANA \(On Premise\)](maintain-business-roles-within-sap-s-4hana-on-premise-d1999cf.md "You can define authorizations for your custom business roles in SAP S/4HANA (On Premise).")

[Restrictions](restrictions-ed62ee4.md "The following is a list of various restrictions provided by Google Drive APIs to support Google Workspace Integration.")

