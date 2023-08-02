<!-- loiob37799034e81433c8312864b0b5a2fab -->

# Onboarding Repository

All documents in CMIS are stored in a repository. Document repositories can be considered as a database. We need to onboard repositories where the document is stored once the SAP Document Management Service instance has been created and bound to an application or a service key has been generated.

There are two types of repositories in Document Management Service:

-   Internal Repositories

    -   Document Management Service's cloud repository.

    -   If you want to add internal repositories, you need the Document Management Service, Repository Option entitlement.

    -   An additional charge is applied for storage.


-   External Repositories

    -   OpenText or SAP S/4HANA DMS repositories are examples of third-party CMIS-compliant repositories.

    -   The repository provider is responsible for providing their own repository, so there are no storage charges.



> ### Note:  
> SAP Document Management Service allows you to onboard multiple repositories in one instance. Depending on your use case, you can onboard multiple internal or external repositories, or a combination of both.



<a name="loiob37799034e81433c8312864b0b5a2fab__section_okh_4rz_hrb"/>

## Onboarding Internal Repository

You've the Document Management Service, Repository Option entitlement in your sub account to onboard internal repository. Because the repository is generated on the go, you need to specify configuration parameters to manage the repository's features and capabilities.

The API for onboarding internal repositories can be found in [SAP Business Accelerator Hub](https://api.sap.com/api/AdminAPI/resource).



### Parameters for configuring internal repositories

The following parameters are needed for onboarding internal repositories:


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

`"displayName"`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

Name of the repository that appears in the application.The external repository is based on the concept of "bring your own repository." To onboard an external repository, you must first maintain the repository information in SAP Destination Service, including the URL, username, and password, and then provide this destination information to our repository onboarding API.



</td>
</tr>
<tr>
<td valign="top">

`"description"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Description of the repository



</td>
</tr>
<tr>
<td valign="top">

`"repositoryType"`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

`internal` 



</td>
</tr>
<tr>
<td valign="top">

`"repositoryCategory"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

`Collaboration`The external repo or `Favorites`

This entry is needed only when you want to create shared folders in the repository. By default, shared folder creation is disabled. For more information, see [Collaboration Repositories](collaboration-repositories-926d32b.md).



</td>
</tr>
<tr>
<td valign="top">

`"isVersionEnabled"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

To maintain multiple versions of your documents.

Acceptable values: true/false

Default value: false



</td>
</tr>
<tr>
<td valign="top">

`"isVirusScanEnabled"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

To scan the documents before you upload them.

Acceptable values:

-   true – enable virus scan and you can upload files only up to 400 MB

-   false \(default value\) – no virus scan and you can upload files of any size




</td>
</tr>
<tr>
<td valign="top">

`"skipVirusScanForLargeFile"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Applicable only if `"isVirusScanEnabled"` is set to true.

Acceptable values:

-   true – no virus scan for uploading files larger than 400 MB

-   false \(default value\) – can't upload files larger than 400 MB




</td>
</tr>
<tr>
<td valign="top">

`"hashAlgorithms"`



</td>
<td valign="top">

Yes



</td>
<td valign="top">

Hashing algorithms to generate a content hash for all your documents. Acceptable values:

-   `MD5`

-   `SHA-1`

-   `SHA-256`

-   `None` \(default value\) – choose this option if you don't want to generate content hash.




</td>
</tr>
<tr>
<td valign="top">

`"externalId"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Unique name for the repository.

The parameter is mandatory only for SAP S/4HANA attachment service scenarios.



</td>
</tr>
<tr>
<td valign="top">

`"isContentBridgeEnabled"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Acceptable values: `true` or `false`

The parameter is mandatory only for SAP S/4HANA attachment service scenarios.



</td>
</tr>
<tr>
<td valign="top">

`"isThumbnailEnabled"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Acceptable values: `true` or `false` 



</td>
</tr>
<tr>
<td valign="top">

`"isEncryptionEnabled"`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

Set the value to `True` if you want to enable encryption to encrypt your sensitive data in the repository. See [Default Encryption via SAP Credential Store](../security-topics/default-encryption-via-sap-credential-store-b978a4d.md).



</td>
</tr>
</table>



<a name="loiob37799034e81433c8312864b0b5a2fab__section_uvl_prz_hrb"/>

## Onboarding External Repository

You can onboard external repositories. The API for onboarding external repositories can be found in [SAP Business Accelerator Hub](https://api.sap.com/api/AdminAPI/resource).



### Parameters for configuring external repositories


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

Description of the repository



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

The value "external" means that you're adding your own repository. To use SAP provided repository, see [Connecting to Document Management Service, Repository Option Using API](connecting-to-document-management-service-repository-option-using-api-d30200e.md).



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

CMIS ID of your repository



</td>
</tr>
<tr>
<td valign="top" rowspan="2">

`"repository":"repositoryParams":"paramName"`and `"repository":"repositoryParams":"paramValue"`



</td>
<td valign="top" rowspan="2">

Optional



</td>
<td valign="top">

`contentServer`

The parameter is needed only for SAP DMS repositories to bypass ABAP layer and directly communicate to the content server to upload documents.



</td>
</tr>
<tr>
<td valign="top">

Content-server destination name

The parameter is needed only for SAP S/4HANA DMS repositories to bypass ABAP layer and directly communicate to the SAP content server to upload documents. It's recommended that the content server configured to allow direct HTTP connections from SAP BTP.

> ### Example:  
> > ### Sample Code:  
> > ```
> > {
> > 
> >     "repository": {
> > 
> >         "displayName": "<Repository Name>",
> > 
> >         "description": "<Description>",
> > 
> >         "repositoryType": "external",
> > 
> >         "repositoryId": "<Repository Id>",
> > 
> >         "repositoryParams": [
> > 
> >             {
> > 
> >                 "paramName": "contentServer",
> > 
> >                 "paramValue": "<Content Server Destination Name>"
> > 
> >             },
> > 
> >             {
> > 
> >                 "paramName": "useContentServerDownload",
> > 
> >                 "paramValue": "<True or False>"
> > 
> >             }
> > 
> >         ]
> > 
> >     },
> > 
> >     "connection": {
> > 
> >         "destinationName": "<Repository Destination Name>"
> > 
> >     }
> > 
> > }
> > ```



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

Unique name for the repository

The parameter is mandatory only for the users of SAP S/4HANA who use Document Management Service, Integration Option for their SAP S/4HANA Attachment service.



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

