<!-- loiof64dcdb6b8b4460cb8dc4e3bece49bc5 -->

# Establishing Trust Configuration Between SAP S/4HANA On-Premise And SAP BTP

To establish SAML trust to the identity providers generated in the SAP S/4HANA On-Premise, import the SAML identity provider metadata to the SAP BTP account.



<a name="loiof64dcdb6b8b4460cb8dc4e3bece49bc5__prereq_asv_42f_l1c"/>

## Prerequisites

-   You've access to the SAP S/4HANA system with the SAP\_BASIS release version higher than **7.40**.

-   You've installed the SAP BTP certificate in your SAP S/4HANA system. For more information about certificates, see [Install Certificates for Communication with SAP BTP](https://help.sap.com/docs/BATCH_RELEASE_HUB_LS_CLOUD/5a6fd89b06e54ea5b82bd8da0e38c9a7/bd6b304124344558bf2e2f97e78eb232.html?locale=en-US).




## Procedure

1.  Log on to your SAP S/4HANA system.

2.  Run the transaction *OA2C\_SAML20*.

3.  Save the data on your device in the form of an XML file.


You can proceed with configurations in SAP BTP cockpit by following the steps:

4.  Log on to your SAP BTP subaccount.

5.  Choose *Security* \> *Trust Configuration* in the side menu.

6.  Choose *New Trust Configuration*.

7.  In the *New Trust Configuration* dialog, choose *Upload* and select the metadata file you generated in step 3.

8.  Enter a *Name* of your choice and choose *Parse* to parse the entered data.

9.  Choose *Save*.

    You've established a trust connection between your subaccount and the ABAP platform in the SAP BTP cockpit. Select the newly created trust, go to the show details area, and double-check that the trust configuration includes the correct *Subject* and *Issuer* values.


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

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-on-premise-and-sap-btp-699a106.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA (on premise) and SAP BTP.")

[Maintain Business Roles Within SAP S/4HANA \(On Premise\)](maintain-business-roles-within-sap-s-4hana-on-premise-d1999cf.md "You can define authorizations for your custom business roles in SAP S/4HANA (On Premise).")

[Restrictions](restrictions-ed62ee4.md "The following is a list of various restrictions provided by Google Drive APIs to support Google Workspace Integration.")

