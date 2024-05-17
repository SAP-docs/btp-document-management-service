<!-- loio26f9c07089fc4ab19372a4313c9ac3a6 -->

# Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA Cloud And SAP BTP

Configure SAML Outbound OAuth configuration between SAP S/4HANA Cloud and SAP BTP.



<a name="loio26f9c07089fc4ab19372a4313c9ac3a6__prereq_x5f_gbb_5tb"/>

## Prerequisites

-   You've established the trust configuration between the ABAP system and SAP BTP. For more information, see [Establishing Trust Configuration Between SAP S/4HANA Cloud And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-cloud-and-sap-btp-66f91a9.md).

-   You've created a service instance and service key of Document Management Service, Integration Option. For more information, see [Creating a Service Instance and Service Key](integration-option-guide/creating-a-service-instance-and-service-key-fe7f1e5.md).

-   From the generated service key, you copied the *ecmservice* URL. Your *ecmservice* URL would look something like`https://api-xyz-dm-gw.cfapps.sap.hana.ondemand.com/`.

-   You've copied the `clientid`, `clientsecret`, and `tokenurl` parameters generated in the same subaccount of Cloud Foundry Environment where Document Management Service, Integration Option instance is created. For more information about creating parameters, see [Create Service Keys Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cdf4f200db3e4c248fa67401937b2f78.html).

-   You've onboarded a repository in Document Management Service, Integration Option. For more information, see [Create a Repository Using the Onboarding API for Google Drive](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md).



## Procedure

1.  Log on to the SAP Fiori launchpad \(SAP S/4HANA Cloud\).

2.  Search for the *Communication Arrangement* app from the SAP Fiori Launchpad.

3.  Choose *New*.

4.  Select the communication scenario `SAP_COM_0190`.

5.  Enter a name for the arrangement in *Arrangement Name*. For example, `Z_TEST_SAP_COM_0190`.

6.  Choose *Create*.

    Communication Arrangement has been created, and you're directed to the communication arrangement page to configure further settings.

7.  In the *Additional Properties* section, maintain the following details:


    <table>
    <tr>
    <th valign="top">

    Property Name
    
    </th>
    <th valign="top">

    Property Value
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *<File Share ID\>*
    
    </td>
    <td valign="top">
    
    `ZTEST`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *<File Share Type\>*
    
    </td>
    <td valign="top">
    
    `2`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *<Repository ID\>*
    
    </td>
    <td valign="top">
    
    `GOOGLE_DRIVE`
    
    </td>
    </tr>
    </table>
    
8.  In *Outbound Communication* section, keep the default values for *SAML2 identifier*.

9.  In *Outbound Services* section, maintain the following details:

    -   *<Path\>*: `/browser`

    -   *<Port\>*: `443`

    > ### Caution:  
    > When connecting your services to SAP BTP services and on-premise systems, credentials are exposed in plain text to the person performing the configuration. Make sure you've operational countermeasures in place to prevent unauthorized copies of credentials from being leaked.

10. Choose *Save*.

    The success message appears once the activation is complete.


**Related Information**  


[Initial Setup](initial-setup-ef91284.md "Before you get started in Document Management Service, Integration Option your SAP BTP account administrator must subscribe to your SAP BTP subaccount to the Document Management Service, Integration Option by performing some preparatory steps.")

[Setting Up a Google Workspace Account](setting-up-a-google-workspace-account-9670f69.md "Create your Google Workspace Account to connect to Document Management Service, Integration Option.")

[Creating HTTP Destinations](creating-http-destinations-2b04ac7.md "Create destinations in your SAP BTP subaccount to connect Google Drive with Document Management Service, Integration Option.")

[Managing Cross-Domain Mapping](managing-cross-domain-mapping-96d2d97.md "Manage cross-domain mapping if your domain is different from the Google Workspace domain.")

[Create a Repository Using the Onboarding API for Google Drive](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md "Create your repository to Document Management Service, Integration Option as it's required for establishing a connection with Google Drive.")

[Supporting CMIS APIs](supporting-cmis-apis-4288da6.md "Following is a list of all supported CMIS (Content Management Interoperability Services) REST APIs.")

[Establishing Trust Configuration Between SAP S/4HANA Cloud And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-cloud-and-sap-btp-66f91a9.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA Cloud, import the SAML identity provider metadata to the Cloud Foundry account.")

[Maintain Business Roles Within the SAP S/4HANA Cloud](maintain-business-roles-within-the-sap-s-4hana-cloud-091973b.md "Create and maintain business roles based on the selected business catalogs.")

[Establishing Trust Configuration Between SAP S/4HANA On-Premise And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-on-premise-and-sap-btp-f64dcdb.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA On-Premise, import the SAML identity provider metadata to the SAP BTP account.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-on-premise-and-sap-btp-699a106.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA (on premise) and SAP BTP.")

[Maintain Business Roles Within SAP S/4HANA \(On Premise\)](maintain-business-roles-within-sap-s-4hana-on-premise-d1999cf.md "You can define authorizations for your custom business roles in SAP S/4HANA (On Premise).")

[Restrictions](restrictions-ed62ee4.md "The following is a list of various restrictions provided by Google Drive APIs to support Google Workspace Integration.")

[Creating a Communication System](creating-a-communication-system-adfc134.md "Create a communication system to link to a communication arrangement.")

