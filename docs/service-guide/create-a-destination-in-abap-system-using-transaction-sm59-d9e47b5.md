<!-- loiod9e47b5112c04d00b4a18a009bdb1e2c -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Create a Destination in ABAP System Using Transaction SM59

Create a destination in transaction SM59 to establish a connection to the SAP Document Management service.



<a name="loiod9e47b5112c04d00b4a18a009bdb1e2c__prereq_jzp_1th_5tb"/>

## Prerequisites

You've created a OAuth 2.0 client and copied the *Profile* and *Configuration Name*. For more information, see [Setting Up SAML Outbound OAuth Configuration Between SAP S/4HANA \(On Premise\) And SAP BTP](setting-up-saml-outbound-oauth-configuration-between-sap-s-4hana-on-premise-and-sap-btp-699a106.md).



## Procedure

1.  Open the transaction SM59.

2.  Choose *Create*, to create a new destination.

    1.  Enter *Destination* name as per your choice. The name must begin with the letter 'Z'. For example, `ZCA325_SAP_COM_0190_0002`.

    2.  Select *Connection Type* as *G HTTP connection to external server*.

    3.  Choose :heavy_check_mark:button.


3.  Navigate to the *Technical Settings*, enter the following details:

    1.  *<Host\>*: first URL from service key \(without *https://*\). For example, `api-ddd-ai-gw.cfapps.sap.hana.ondemand.com`
    2.  *<Port\>*: `443`
    3.  *<Path Prefix\>*: */browser*

4.  Navigate to the *Logon & Security* tab, perform the following steps:

    1.  Choose *OAuth Settings*.

    2.  Click on <span class="SAP-icons"></span> value-helpicon.

    3.  Choose *Profl* that you created.

    4.  Scroll down to *Security Options*. Set the *<SSL\>* client to `Active` and select *DFAULT SSL Client \(Standard\)* as default settings.


5.  Choose :floppy_disk: to save the destination.

6.  Choose the *Connection Test* option at the top of the page, and ignore warning message. The returned HTTP status should be ***200***.

    When you run the *Connection Test*, the *Response Text* section shows ***200 OK*** as the response code, as well as the repositories that have been onboarded for the connected service instance.


**Related Information**  


[Run the Transaction V\_CMIS\_L\_FS](run-the-transaction-v-cmis-l-fs-bdac58c.md "Run the transaction to complete the configuration in ABAP on-premise environment")

