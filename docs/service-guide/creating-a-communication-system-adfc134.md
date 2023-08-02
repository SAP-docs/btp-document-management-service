<!-- loioadfc134f8c2c4acd8d1135e5154b44b5 -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Creating a Communication System

Create a communication system to link to a communication arrangement.



<a name="loioadfc134f8c2c4acd8d1135e5154b44b5__prereq_m4k_pq3_5tb"/>

## Prerequisites

-   You've an admin access to the SAP S/4HANA Cloud system.

-   You've already Created a Communication Arrangement. For more information, see [Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA Cloud And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-cloud-and-sap-btp-26f9c07.md).




<a name="loioadfc134f8c2c4acd8d1135e5154b44b5__steps_fn1_jq3_5tb"/>

## Procedure

1.  Log on to the SAP Fiori launchpad \(SAP S/4HANA Cloud\).

2.  Search for the *Communication Arrangement* and select the *Arragement Name* from the list.

3.  Navigate to *Common Data* section. To create a new communication system, choose *New*.

4.  On the *New Communication System* screen, enter the following details:

    -   *<System ID\>*: Enter the system ID.

    -   *<System Name\>*: Enter a descriptive name for the system.

5.  Choose *Create*.

6.  Under the *General tab*, enter the following details in the *Technical Data* section:

    -   *<Host Name\>*: Enter the first *ecmservice* URL from the service key without *https://*. For example, `api-ddd-ai-gw.cfapps.sap.hana.ondemand.com`

    -   *<Port\>*: Use the default value, for example, `443`.


7.  Enter the Authorization and Token Endpoints under *OAuth 2.0 Settings*.

    1.  To enter *Authorization Endpoint*, copy the authentication URL listed under *uaa* of your service key. Delete `https://` from the URL and add `/oauth/authorize`. For example, `<subaccountname>.authentication.sap.hana.ondemand.com/oauth/authorize`

    2.  To enter *Token Endpoint*, enter the URL that you copied while establishing trust configuration between ABAP system and SAP BTP. For more information, see [Using SAML Metadata from the Cloud Foundry Account to Copy Location Key](using-saml-metadata-from-the-cloud-foundry-account-to-copy-location-key-74c177a.md).

        > ### Example:  
        > `<subaccountname>.authentication.sap.hana.ondemand.com/oauth/token/alias/<account>`

    3.  In the *Audience* field, copy the authentication URL with *https://* listed under *uaa* of your service key. For example, `https://<subaccountname>.authentication.sap.hana.ondemand.com`


8.  Scroll down to the section *User for Outbound Communication* and choose :heavy_plus_sign: to create new outbound user.

9.  In the *New Outbound User* dialog, select *OAuth 2.0* in *Authentication Method* field.

10. Set *Basic* for *Client Authentication*.

11. Enter `client ID` that you copied from the service key in the *OAuth 2.0 Client ID* field.

12. Enter `clientsecret` that you copied from the service key in the *Client Secret* field.

13. Choose *Create*.

14. Select the *Save* option at the bottom of the page to save the communication system.


