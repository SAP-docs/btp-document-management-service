<!-- loio96d2d978006c4aa18c9680cac9c0369b -->

# Managing Cross-Domain Mapping

Manage cross-domain mapping if your domain is different from the Google Workspace domain.



## Prerequisites

-   You are an Admin for Document Management Service, Integration Option via the `SDM_Admin` scope.

-   You've generated a JSON Web Token \(JWT\) that serves as your authorization for making API calls. For more information, see [Generate a JSON Web Token](integration-option-guide/generate-a-json-web-token-bff9fd6.md).

-   You've copied the *URI* value from the service key of Document Management Service, Integration Option. For more information, see [Creating a Service Instance and Service Key](integration-option-guide/creating-a-service-instance-and-service-key-fe7f1e5.md).

-   You've created an HTTP destination and added the following additional property. See [Creating HTTP Destinations](creating-http-destinations-2b04ac7.md).


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
    
    `google.default_domain`
    
    </td>
    <td valign="top">
    
    Enter the domain. For example, `abcworkspace.com`.
    
    </td>
    </tr>
    </table>
    

If the domains on the customer and Google Workspace are different. Then we map the user account on the customer system to the domain on Google Workspace. For example, if you're using the domain *abc.com* \(jhon.thane1@abc.com\) and have a Google Workspace account with the domain *abcworkspace.com* \(jhon.thane1@abcworkspace.com\), then use the following request.



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/configs</code>

**HTTP Method:***POST*

**Permissions:** Admin for Document Management Service, Integration Option via the `SDM_Admin` scope

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](integration-option-guide/generate-a-json-web-token-bff9fd6.md)\)

**Body**

> ### Sample Code:  
> ```json
> 
> {
> "configName" : "isCrossDomainMappingAllowed",
> "configValue" : "true"
> }
> 
> ```

> ### Note:  
> To disable the cross-domain check, use the *POST* request but set the `configValue` to `false`. The `configValue` is set to `false` by default.
> 
> > ### Sample Code:  
> > ```json
> > 
> > {
> > "configName" : "isCrossDomainMappingAllowed",
> > "configValue" : "false"
> > }
> > 
> > ```

> ### Caution:  
> When connecting your services to SAP BTP services and on-premise systems, credentials are exposed in plain text to the person performing the configuration. Make sure that you have operational countermeasures in place to prevent unauthorized copies of credentials from being leaked.

**Related Information**  


[Initial Setup](initial-setup-ef91284.md "Before you get started in Document Management Service, Integration Option your SAP BTP account administrator must subscribe to your SAP BTP subaccount to the Document Management Service, Integration Option by performing some preparatory steps.")

[Setting Up a Google Workspace Account](setting-up-a-google-workspace-account-9670f69.md "Create your Google Workspace Account to connect to Document Management Service, Integration Option.")

[Creating HTTP Destinations](creating-http-destinations-2b04ac7.md "Create destinations in your SAP BTP subaccount to connect Google Drive with Document Management Service, Integration Option.")

[Create a Repository Using the Onboarding API for Google Drive](create-a-repository-using-the-onboarding-api-for-google-drive-90faa8c.md "Create your repository to Document Management Service, Integration Option as it's required for establishing a connection with Google Drive.")

[Supporting CMIS APIs](supporting-cmis-apis-4288da6.md "Following is a list of all supported CMIS (Content Management Interoperability Services) REST APIs.")

[Establishing Trust Configuration Between SAP S/4HANA Cloud And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-cloud-and-sap-btp-66f91a9.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA Cloud, import the SAML identity provider metadata to the Cloud Foundry account.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA Cloud And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-cloud-and-sap-btp-26f9c07.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA Cloud and SAP BTP.")

[Maintain Business Roles Within the SAP S/4HANA Cloud](maintain-business-roles-within-the-sap-s-4hana-cloud-091973b.md "Create and maintain business roles based on the selected business catalogs.")

[Establishing Trust Configuration Between SAP S/4HANA On-Premise And SAP BTP](establishing-trust-configuration-between-sap-s-4hana-on-premise-and-sap-btp-f64dcdb.md "To establish SAML trust to the identity providers generated in the SAP S/4HANA On-Premise, import the SAML identity provider metadata to the SAP BTP account.")

[Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-on-premise-and-sap-btp-699a106.md "Configure SAML Outbound OAuth configuration between SAP S/4HANA (on premise) and SAP BTP.")

[Maintain Business Roles Within SAP S/4HANA \(On Premise\)](maintain-business-roles-within-sap-s-4hana-on-premise-d1999cf.md "You can define authorizations for your custom business roles in SAP S/4HANA (On Premise).")

[Restrictions](restrictions-ed62ee4.md "The following is a list of various restrictions provided by Google Drive APIs to support Google Workspace Integration.")

