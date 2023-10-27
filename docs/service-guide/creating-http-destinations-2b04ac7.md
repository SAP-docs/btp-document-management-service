<!-- loio2b04ac7ce43647b8a0cca2c28e1bef52 -->

# Creating HTTP Destinations

Create destinations in your SAP BTP subaccount to connect Google Drive with Document Management Service, Integration Option.



<a name="loio2b04ac7ce43647b8a0cca2c28e1bef52__prereq_a13_3qd_qtb"/>

## Prerequisites

-   You've added entitlements for Document Management Service, Integration Option. For more information about entitlements, see [Configure Entitlements and Quotas for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).

-   You've created a service instance and service key of Document Management Service, Integration Option. For more information, see [Creating a Service Instance and Service Key](integration-option-guide/creating-a-service-instance-and-service-key-fe7f1e5.md).

-   The following authorizations have been added to your subaccount. For more information, see [Configuring User Access](web-app-guide/configuring-user-access-66e4071.md).


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
    
    Admin or Repository Management APIs
    
    </td>
    <td valign="top">
    
    `SDM_Admin`
    
    </td>
    </tr>
    </table>
    



## Procedure

1.  Log on to the SAP BTP cockpit and navigate to your subaccount.

2.  In the left pane, navigate to *Connectivity* \> *Destinations*.

3.  Choose *New Destination*.

4.  In the *Destination Configuration* section, provide values in the following fields:


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Name*
    
    </td>
    <td valign="top">
    
    Choose a name for your destination.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Type*
    
    </td>
    <td valign="top">
    
    HTTP
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Description*
    
    </td>
    <td valign="top">
    
    Optional: Provide a description for your reference
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *URL*
    
    </td>
    <td valign="top">
    
    Fill in the Google Drive URL.

    > ### Example:  
    > `https://www.googleapis.com/drive/v3`


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Proxy Type*
    
    </td>
    <td valign="top">
    
    Internet
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Authentication*
    
    </td>
    <td valign="top">
    
    No Authentication
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Additional Properties*
    
    </td>
    <td valign="top">
    
    As key-value pairs, enter the values from your service account JSON file with the prefix "google." in the keys followed by the pattern:`Key1=Value1, Key2=Value2,...`

    > ### Note:  

    You can check the JSON file that you downloaded when you created the service account access. For more information, see [Configure Service Account Access](configure-service-account-access-9774430.md).
    
    </td>
    </tr>
    </table>
    
    The following additional properties must be included when you create an HTTP destination.


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
    
    `google.auth_provider_x509_cert_url`
    
    </td>
    <td valign="top">
    
    An *auth\_provider\_x509\_cert\_url* obtained from a JSON file.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `google.auth_uri`
    
    </td>
    <td valign="top">
    
    The Google authentication URI obtained from a JSON file.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `google.client_email`
    
    </td>
    <td valign="top">
    
    A client email obtained from a JSON file.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `google.client_id`
    
    </td>
    <td valign="top">
    
    A client ID obtained from a JSON file.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `google.client_x509_cert_url`
    
    </td>
    <td valign="top">
    
    A client X509 certificate URL obtained from a JSON file.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `google.private_key`
    
    </td>
    <td valign="top">
    
    Enter the Google Cloud private key.

    > ### Remember:  
    > Don't include double quotes [“\] in the private key. Make sure to copy the key without it.
    > 
    > > ### Example:  
    > > Your private key looks like the following:
    > > 
    > > ```
    > > 
    > > -----BEGIN PRIVATE KEY----
    > > 
    > > \nMIIEvQIBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQCfp4PTx3ezoyXT\n
    > > xP5mtFk3tQ6Z2mvPo/PEwKJidaUQnEz5kQqZynGb1OZX9Kd7JJb6l0zjb5S2NJ/O\n/Fg+55Xlb5y\nMy+kxM+EHmthpHoBDEZQEnM=\n
    > > -----END PRIVATE KEY-----\n
    > > ```


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `google.private_key_id`
    
    </td>
    <td valign="top">
    
    A private key ID obtained from a JSON file.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `google.project_id`
    
    </td>
    <td valign="top">
    
    A project ID obtained from a JSON file.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `google.token_uri`
    
    </td>
    <td valign="top">
    
    A token URI obtained from a JSON file.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `google.type`
    
    </td>
    <td valign="top">
    
    `service_account`
    
    </td>
    </tr>
    </table>
    
    > ### Caution:  
    > When connecting your services to SAP BTP services and on-premise systems, credentials are exposed in plain text to the person performing the configuration. Make sure that you've operational countermeasures in place to prevent unauthorized copies of credentials from being leaked.

5.  Select the *Use default JDK truststore* checkbox.

6.  Choose *Save*.


**Related Information**  


[Setting Up a Google Workspace Account](setting-up-a-google-workspace-account-9670f69.md "Create your Google Workspace Account to connect to Document Management Service, Integration Option.")

[Managing Cross-Domain Mapping](managing-cross-domain-mapping-96d2d97.md "Manage cross-domain mapping if your domain is different from the Google Workspace domain.")

[Create a Repository Using the Onboarding API for Google Drive](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md "Create your repository to Document Management Service, Integration Option as it's required for establishing a connection with Google Drive.")

[Supporting CMIS APIs](supporting-cmis-apis-4288da6.md "Following is a list of all supported CMIS (Content Management Interoperability Services) REST APIs.")

[Establishing Trust Configuration Between SAP S/4HANA Cloud And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-cloud-and-sap-btp-66f91a9.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA Cloud, import the SAML identity provider metadata to the Cloud Foundry account.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA Cloud And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-cloud-and-sap-btp-26f9c07.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA Cloud and SAP BTP.")

[Maintain Business Roles Within the SAP S/4HANA Cloud](maintain-business-roles-within-the-sap-s-4hana-cloud-091973b.md "Create and maintain business roles based on the selected business catalogs.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-on-premise-and-sap-btp-699a106.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA (on premise) and SAP BTP.")

[Maintain Business Roles Within SAP S/4HANA \(On Premise\)](maintain-business-roles-within-sap-s-4hana-on-premise-d1999cf.md "You can define authorizations for your custom business roles in SAP S/4HANA (On Premise).")

[Restrictions](restrictions-ed62ee4.md "The following is a list of various restrictions provided by Google Drive APIs to support Google Workspace Integration.")

[Connecting Your Own Repository to Document Management Service, Integration Option](integration-option-guide/connecting-your-own-repository-to-document-management-service-integration-option-21bd278.md "Connect your choice of CMIS-compliant, on-premise, or cloud repository to Document Management Service, Integration Option using REST APIs.")

