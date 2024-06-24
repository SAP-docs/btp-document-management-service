<!-- loio699a106cf3984396be7d575ec880f3e0 -->

# Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP

Configure SAML Outbound OAuth configuration between SAP S/4HANA \(on premise\) and SAP BTP.



<a name="loio699a106cf3984396be7d575ec880f3e0__prereq_x5f_gbb_5tb"/>

## Prerequisites

-   You've established the trust configuration between the ABAP system and SAP BTP. For more information, see [Establishing Trust Configuration Between SAP S/4HANA On-Premise And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-on-premise-and-sap-btp-f64dcdb.md).

-   You've created a service instance and service key of Document Management Service, Integration Option. For more information, see [Creating a Service Instance and Service Key](integration-option-guide/creating-a-service-instance-and-service-key-fe7f1e5.md).

-   From the generated service key, you copied the ecmservice URL. Your ecmservice URL would look something like`https://api-xyz-dm-gw.cfapps.sap.hana.ondemand.com/`.

-   You've copied the `clientid`, `clientsecret`, and `tokenurl` parameters generated in the same subaccount of Cloud Foundry Environment where Document Management Service, Integration Option instance is created. For more information about creating parameters, see [Create Service Keys Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cdf4f200db3e4c248fa67401937b2f78.html).

-   You've onboarded a repository in Document Management Service, Integration Option. For more information, see [Create a Repository Using the Onboarding API for Google Drive](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md).



## Procedure

1.  Open the ABAP client.

2.  Start transaction `OA2C_CONFIG` to access OAuth 2.0 Clients.

3.  To create an *OAuth 2.0 client*, choose *Create*. A popup with the configuration UI appears.

4.  Select *OAuth 2.0 Client Profile* as `CMIS_FS_SDM_SAML`.

5.  Enter the *Configuration Name* as per your requirement.

6.  Enter *OAuth 2.0 Client ID*. Take the client ID from the service key that you've generated in the SAP BTP cockpit.

7.  Choose *OK*.

    The OAuth 2.0 client profile and the client ID appear in the *General Settings* section of the new OAuth 2.0 client.

8.  Under *General Settings*, enter the *Client Secret*. To know your `Client ID` and `Client Secret`, see **Prerequisites** .

9.  Enter the Authorization and Token Endpoints under *Authorization Server Settings*.

    1.  To enter *Authorization Endpoint*, copy the authentication URL listed under *uaa* of your service key. Delete `https://` from the URL and add `/oauth/authorize`. For example, `<subaccountname>.authentication.sap.hana.ondemand.com/oauth/authorize`

    2.  To enter *Token Endpoint*, enter the URL that you copied while establishing trust configuration between ABAP system and SAP BTP. For more information, see [Using SAML Metadata from the Cloud Foundry Account to Copy Location Key](using-saml-metadata-from-the-cloud-foundry-account-to-copy-location-key-74c177a.md).

        > ### Example:  
        > `<subaccountname>.authentication.sap.hana.ondemand.com/oauth/token/alias/<account>`


10. Under *Access Settings*, keep the default settings and on *SAML 2.0 Bearer Assertion*, click the checkbox.

    1.  Copy the authentication URL listed under *uaa* of your service key and enter in the field *SAML 2.0 Audience*

        > ### Example:  
        > `https://<subaccountname>.authentication.sap.hana.ondemand.com`


    > ### Caution:  
    > When connecting your services to SAP BTP services and on-premise systems, credentials are exposed in plain text to the person performing the configuration. Make sure you've operational countermeasures in place to prevent unauthorized copies of credentials from being leaked.

11. Choose *Save*.

    An OAuth 2.0 client has been created.


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

[Maintain Business Roles Within SAP S/4HANA \(On Premise\)](maintain-business-roles-within-sap-s-4hana-on-premise-d1999cf.md "You can define authorizations for your custom business roles in SAP S/4HANA (On Premise).")

[Restrictions](restrictions-ed62ee4.md "The following is a list of various restrictions provided by Google Drive APIs to support Google Workspace Integration.")

[Create a Destination in ABAP System Using Transaction SM59](create-a-destination-in-abap-system-using-transaction-sm59-d9e47b5.md "Create a destination in transaction SM59 to establish a connection to the SAP Document Management service.")

