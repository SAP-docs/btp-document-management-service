<!-- loioed62ee4aa36b4452bdb39b9250fcb7f2 -->

# Restrictions

The following is a list of various restrictions provided by Google Drive APIs to support Google Workspace Integration.

> ### Remember:  
> We provide this information to make it easier for you to gain access to all Google Drive API limitations. The best place to find accurate and up-to-date information is Google's help content available on their support portal.

-   A shared drive has certain restrictions, such as the maximum number of items, the maximum number of daily uploads, file sharing, folders, and so on. For more information, see [Google Workspace Help](https://support.google.com/a/answer/7338880).

-   There are several restrictions to the size of documents, spreadsheets, presentations, and any other files you store in Google Drive. For more information, see [Google Drive Help](https://support.google.com/drive/answer/37603?hl=en).

-   A given file within a Shared Drive can be directly shared with a maximum number of groups. For more information, see[Google Workspace Help](https://support.google.com/a/answer/7338880) and [Share folders in Google Drive](https://support.google.com/drive/answer/7166529).




<a name="loioed62ee4aa36b4452bdb39b9250fcb7f2__section_cpt_zkw_5tb"/>

## Restrictions on Properties for Secondary Types

Custom properties for secondary types have the following limits:

-   Maximum of 100 custom properties per file, totaled from all sources.

-   Maximum of 124-bytes size per property \(including both key and value\) string in UTF-8 encoding. For example, a property with a key that is 10 characters long can only have 114 characters in the value. A property that requires 100 characters for the value can use up to 24 characters for the key.


For more information, see [Limitations on Custom File Properties](https://developers.google.com/drive/api/guides/properties).



<a name="loioed62ee4aa36b4452bdb39b9250fcb7f2__section_ork_dlw_5tb"/>

## Restrictions on Supported Queries

The query support from Google is subject to some restrictions.

-   Limited list of fields acceptable in *Where section*: `cmis:name`, `cmis:objectId`, `cmis:parentId`, `cmis:createdBy`, `cmis:creationDate`, and `cmis:lastModificationDate`.

-   Limited list of fields acceptable in *From section*: `cmis:document` and `cmis:folder`

-   Limited list of fields acceptable in *Order By section*: `cmis:creationDate`, `cmis:lastModificationDate`, `cmis:baseTypeId`, and `cmis:name`.

-   The contains\(like\) operator only performs prefix matching for a name term.

-   Maximum of 1000 files returned by Google per page.

-   If the number of files is more than 1 million, ordering isn't provided.

-   A list of shared drives can't be sorted by **orderBy**.




If you're interested in learning FAQs about managing Google Drive for an organization or team. See [Managing Google Drive Help](https://support.google.com/a/answer/2490100#zippy=%2Chow-many-items-can-i-have-directly-in-a-folder).

**Related Information**  


[Initial Setup](initial-setup-ef91284.md "Before you get started in Document Management Service, Integration Option your SAP BTP account administrator must subscribe to your SAP BTP subaccount to the Document Management Service, Integration Option by performing some preparatory steps.")

[Setting Up a Google Workspace Account](setting-up-a-google-workspace-account-9670f69.md "Create your Google Workspace Account to connect to Document Management Service, Integration Option.")

[Creating HTTP Destinations](creating-http-destinations-2b04ac7.md "Create destinations in your SAP BTP subaccount to connect Google Drive with Document Management Service, Integration Option.")

[Managing Cross-Domain Mapping](managing-cross-domain-mapping-96d2d97.md "Manage cross-domain mapping if your domain is different from the Google Workspace domain.")

[Create a Repository Using the Onboarding API for Google Drive](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md "Create your repository to Document Management Service, Integration Option as it's required for establishing a connection with Google Drive.")

[Supporting CMIS APIs](supporting-cmis-apis-4288da6.md "Following is a list of all supported CMIS (Content Management Interoperability Services) REST APIs.")

[Establishing Trust Configuration Between SAP S/4HANA Cloud And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-cloud-and-sap-btp-66f91a9.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA Cloud, import the SAML identity provider metadata to the Cloud Foundry account.")

[Setting Up Outbound OAuth Configuration Between SAP BTP and SAP S/4HANA Cloud](setting-up-outbound-oauth-configuration-between-sap-btp-and-sap-s-4hana-cloud-26f9c07.md "Configure SAML Outbound OAuth configuration between SAP BTP and SAP S/4HANA Cloud.")

[Setting Up Inbound Configuration Between SAP BTP and SAP S/4HANA Cloud](setting-up-inbound-configuration-between-sap-btp-and-sap-s-4hana-cloud-5aa38f2.md "Configure Inbound configuration between SAP BTP and SAP S/4HANA Cloud.")

[Maintain Business Roles Within the SAP S/4HANA Cloud](maintain-business-roles-within-the-sap-s-4hana-cloud-091973b.md "Create and maintain business roles based on the selected business catalogs.")

[Establishing Trust Configuration Between SAP S/4HANA On-Premise And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-on-premise-and-sap-btp-f64dcdb.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA On-Premise, import the SAML identity provider metadata to the SAP BTP account.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-on-premise-and-sap-btp-699a106.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA (on premise) and SAP BTP.")

[Maintain Business Roles Within SAP S/4HANA \(On Premise\)](maintain-business-roles-within-sap-s-4hana-on-premise-d1999cf.md "You can define authorizations for your custom business roles in SAP S/4HANA (On Premise).")

