<!-- loio66f91a966adb4627acb0ac5ee0d9613f -->

# Establishing Trust Configuration Between SAP S/4HANA Cloud And SAP BTP

To establish SAML trust to the identity providers generated in the SAP S/4HANA Cloud, import the SAML identity provider metadata to the Cloud Foundry account.



## Procedure

1.  Log on to your SAP S/4HANA cloud.

2.  In the search box, type *Communication System* and open it.

3.  You can find the system by navigating to the *Own SAP Cloud System* filter and choose *Yes* \> *Go*.

    As a result of filtering the search, you can be able to see a list of available communication systems.

4.  Choose a *Communication System*. Click on *Download SAML 2.0 Metadata* in the *Technical Data* section and save the file locally.


You can proceed with configurations in SAP BTP cockpit by following the steps:

5.  Log on to your SAP BTP subaccount.

6.  Choose *Security* \> *Trust Configuration* in the side menu.

7.  Choose *New Trust Configuration*.

8.  In the *New Trust Configuration* dialog, choose *Upload* and select the metadata file you generated in step 4.

9.  Enter a *Name* of your choice and choose *Parse* to parse the entered data.

10. Choose *Save*.

    You've established a trust connection between your subaccount and the ABAP platform in SAP BTP cockpit. Select the newly created trust, go to the show details area, and double-check that the trust configuration includes the correct *Subject* and *Issuer* values.


**Related Information**  


[Setting Up a Google Workspace Account](setting-up-a-google-workspace-account-9670f69.md "Create your Google Workspace Account to connect to Document Management Service, Integration Option.")

[Creating HTTP Destinations](creating-http-destinations-2b04ac7.md "Create destinations in your SAP BTP subaccount to connect Google Drive with Document Management Service, Integration Option.")

[Managing Cross-Domain Mapping](managing-cross-domain-mapping-96d2d97.md "Manage cross-domain mapping if your domain is different from the Google Workspace domain.")

[Create a Repository Using the Onboarding API for Google Drive](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md "Create your repository to Document Management Service, Integration Option as it's required for establishing a connection with Google Drive.")

[Supporting CMIS APIs](supporting-cmis-apis-4288da6.md "Following is a list of all supported CMIS (Content Management Interoperability Services) REST APIs.")

[Setting Up Outbound OAuth Configuration Between SAP BTP and SAP S/4HANA Cloud](setting-up-outbound-oauth-configuration-between-sap-btp-and-sap-s-4hana-cloud-26f9c07.md "Configure SAML Outbound OAuth configuration between SAP BTP and SAP S/4HANA Cloud.")

[Setting Up Inbound Configuration Between SAP BTP and SAP S/4HANA Cloud](setting-up-inbound-configuration-between-sap-btp-and-sap-s-4hana-cloud-5aa38f2.md "Configure Inbound configuration between SAP BTP and SAP S/4HANA Cloud.")

[Maintain Business Roles Within the SAP S/4HANA Cloud](maintain-business-roles-within-the-sap-s-4hana-cloud-091973b.md "Create and maintain business roles based on the selected business catalogs.")

[Establishing Trust Configuration Between SAP S/4HANA On-Premise And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-on-premise-and-sap-btp-f64dcdb.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA On-Premise, import the SAML identity provider metadata to the SAP BTP account.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-on-premise-and-sap-btp-699a106.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA (on premise) and SAP BTP.")

[Maintain Business Roles Within SAP S/4HANA \(On Premise\)](maintain-business-roles-within-sap-s-4hana-on-premise-d1999cf.md "You can define authorizations for your custom business roles in SAP S/4HANA (On Premise).")

[Restrictions](restrictions-ed62ee4.md "The following is a list of various restrictions provided by Google Drive APIs to support Google Workspace Integration.")

[Working with Users](working-with-users-1c946cc.md "You can create required users in your subaccount. When creating a user, you've to provide the identity provider with which the user can be stored.")

[Using SAML Metadata from the Cloud Foundry Account to Copy Location Key](using-saml-metadata-from-the-cloud-foundry-account-to-copy-location-key-74c177a.md "Get the SAML service provider metadata from your Cloud Foundry account.")

