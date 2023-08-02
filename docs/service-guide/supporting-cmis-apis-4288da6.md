<!-- loio4288da62468349a593dd7c090a0d2d08 -->

# Supporting CMIS APIs

Following is a list of all supported CMIS \(Content Management Interoperability Services\) REST APIs.




<table>
<tr>
<th valign="top">

API Name



</th>
<th valign="top">

Details



</th>
</tr>
<tr>
<td valign="top">

`createDocument`



</td>
<td valign="top">

Creates a document in the specified location inside repository. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/CreateDocumentApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`createDocumentFromSource`



</td>
<td valign="top">

Creates copy of document from the source folder into a targeted folder without changing any properties of the document. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/CreateDocumentFromSourceApi/overview)



</td>
</tr>
<tr>
<td valign="top">

`getContentStream`



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

`getRepositories` and `getRepositoryInfo`



</td>
<td valign="top">

Returns a list of Content Management Interoperability Services\(CMIS\) repositories available for the instance. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/ServiceApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`getObject`



</td>
<td valign="top">

The API provides the information for the specified object where the object can be of folder, link, document type. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/ServiceApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`getChildren`



</td>
<td valign="top">

The API returns the list of child objects contained in the specified folder. It provides us information about the immediate children of specified object. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/GetChildrenApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`updateType`



</td>
<td valign="top">

Update properties of object present inside repository. For more information, see published APIs on the [SSAP Business Accelerator Hub](https://api.sap.com/api/UpdatePropertiesApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`deleteType`



</td>
<td valign="top">

Update properties of object present inside repository. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/UpdatePropertiesApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`getProperties`



</td>
<td valign="top">

Provides properties of a given object. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/GetPropertiesApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`updateProperties`



</td>
<td valign="top">

Update properties of object present inside repository. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/UpdatePropertiesApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`createFolder`



</td>
<td valign="top">

Creates a folder in the specified location of a repository. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/GetPropertiesApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`getObjectParents`



</td>
<td valign="top">

The API provides the information for the specified object where the object can be of folder, link, document type. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/ServiceApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`getFolderParent`



</td>
<td valign="top">

Provides parent folder object for the given object. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/GetParentApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`deleteObject`



</td>
<td valign="top">

Delete the created object having unique object ID. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/DeleteObjectApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`deleteTree`



</td>
<td valign="top">

Deletes the specified folder object and all of its child- and descendant-objects. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/DeleteTreeApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`setContentStream`



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

`createSecondaryType` or `createType`



</td>
<td valign="top">

A secondary type defines a set of properties that can be dynamically added to and removed from objects. That is, an object can get and lose additional properties that aren't defined by its primary type during its lifetime. Multiple secondary types can be applied to the same object at the same time. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/CreateSecondaryTypeApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`updateSecondaryType`



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

`deleteSecondaryType`



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

`getTypeDefinition`



</td>
<td valign="top">

Provides the definition of the specified object type. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/GetTypeDefinitionApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`getTypeDescendants`



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

`moveObject`



</td>
<td valign="top">

Moves an object from source folder to the targeted folder. For more information, see published APIs on the [SAP Business Accelerator Hub](https://api.sap.com/api/MoveObjectApi/overview).



</td>
</tr>
<tr>
<td valign="top">

`getObjectByPath`



</td>
<td valign="top">

 



</td>
</tr>
</table>

**Related Information**  


[Setting Up a Google Workspace Account](setting-up-a-google-workspace-account-9670f69.md "Create your Google Workspace Account to connect to Document Management Service, Integration Option.")

[Creating HTTP Destinations](creating-http-destinations-2b04ac7.md "Create destinations in your SAP BTP subaccount to connect Google Drive with Document Management Service, Integration Option.")

[Managing Cross-Domain Mapping](managing-cross-domain-mapping-96d2d97.md "Manage cross-domain mapping if your domain is different from the Google Workspace domain.")

[Create a Repository Using the Onboarding API for Google Drive](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md "Create your repository to Document Management Service, Integration Option as it's required for establishing a connection with Google Drive.")

[Establishing Trust Configuration Between SAP S/4HANA Cloud And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-cloud-and-sap-btp-66f91a9.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA Cloud, import the SAML identity provider metadata to the Cloud Foundry account.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA Cloud And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-cloud-and-sap-btp-26f9c07.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA Cloud and SAP BTP.")

[Maintain Business Roles Within the SAP S/4HANA Cloud](maintain-business-roles-within-the-sap-s-4hana-cloud-091973b.md "Create and maintain business roles based on the selected business catalogs.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-on-premise-and-sap-btp-699a106.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA (on premise) and SAP BTP.")

[Maintain Business Roles Within SAP S/4HANA \(On Premise\)](maintain-business-roles-within-sap-s-4hana-on-premise-d1999cf.md "You can define authorizations for your custom business roles in SAP S/4HANA (On Premise).")

[Restrictions](restrictions-ed62ee4.md "The following is a list of various restrictions provided by Google Drive APIs to support Google Workspace Integration.")

