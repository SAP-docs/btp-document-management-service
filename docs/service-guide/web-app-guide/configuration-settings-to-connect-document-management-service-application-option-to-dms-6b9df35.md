<!-- loio6b9df35e0f1e46db8a4abd75d6283937 -->

# Configuration Settings to Connect Document Management Service, Application Option to DMS

This topic describes the steps to connect Document Management Service, Application Option to **Document Management \(DMS\)** in SAP S/4HANA. As a prerequisite, you have performed the following steps:

-   You've created an SAP Business Technology Platform \(BTP\) account.

-   You have installed the cloud connector. For more information, see [Cloud Connector](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/e6c7616abb5710148cfcf3e75d96d596.html).
-   You've maintained the configuration settings for DMS. For more information, see [Configuration Settings for SAP Document Management System \(DMS\)](https://help.sap.com/viewer/1317b7d3a93c4763a041b49532666fd7/2021.000/en-US/6ec4f07818b64868bdee115ca83f7109.html).




<a name="loio6b9df35e0f1e46db8a4abd75d6283937__section_lrg_43s_mqb"/>

## Adding a Cloud Foundry Subaccount to the Cloud Connector

1.  Navigate to your SAP BTP cloud foundry subaccount and click on the Information \(i\) icon below the subaccount title.

2.  Copy the subaccount *ID*.

3.  Log on to the cloud connector.

    > ### Note:  
    > To log on to the cloud connector, in the web browser, enter `https://<hostname>:<port>`.
    > 
    > -   `<hostname>` refers to the machine on which the cloud connector has been installed. If installed on your machine, you can enter `localhost`.
    > 
    > -   `<hostname>`refers to the machine on which the cloud connector has been installed. If installed on your machine, you can enter `localhost`.

    The system displays the *Cloud Connector Administration* screen.

4.  In the *Cloud Connector Administration* screen, click on *Add Subaccount*.
5.  Enter the *Region*. For example, `cf.eu10.hana.ondemand.com` for Europe \(Frankfurt\) – AWS.
6.  Enter the *Subaccount*.
7.  Enter your SAP BTP *Login E-Mail* and *Password* and save the configuration. Optionally, enter the *Location ID*.



## Adding a System Mapping

Add a connection to the ABAP system in the cloud connector.

1.  Navigate to the *Cloud Connector Administration* screen.

2.  Under your subaccount, choose the *Cloud To On-Premise* option in the left panel.

3.  In the *Cloud To On-Premise* screen, click on the Add \(*\+*\) button.

    The system displays the *Add System Mapping* dialog box.

4.  Select *ABAP System* in *Back-end Type* and then choose *Next*.

5.  Choose *HTTPS* in *Protocol* and then choose *Next*.

6.  Enter the Internal Host and Port of your ABAP system. To find the internal host and port of your ABAP system, execute transaction `SMICM` in the backend ABAP system and click on *Services* and copy the Host and Port for HTTPS protocol.

7.  Enter the virtual host and port and then choose *Next*.

    > ### Note:  
    > For Document Management, the internal host and virtual host should be same in order for the integration to work.

8.  Choose *None* in *Principal Type* and then choose *Next*.

9.  Choose *Use Virtual Host* in *Host in Request Header* and then choose *Next*.
10. Choose *Finish*.




<a name="loio6b9df35e0f1e46db8a4abd75d6283937__section_ddf_w5c_jqb"/>

## Adding a Resource

After setting up a connection to the host, add a resource to enable the connection through the cloud connector.

1.  In the *Access Control* tab of Cloud Connector, under the *Resources* section, choose Add \(*\+*\).

2.  In the *Add Resource* dialog box, provide the *URL Path* `/sap/bc/mcm/json`.

3.  Select *Access Policy* as path and all sub paths.

4.  Save your changes.




<a name="loio6b9df35e0f1e46db8a4abd75d6283937__section_glh_w5c_jqb"/>

## Creating a Destination in SAP Business Technology Platform \(SAP BTP\)

In your web browser, log on to the SAP BTP cockpit, and navigate to your cloud foundry subaccount.

1.  Navigate to *Connectivity* \> *Destinations*.

2.  Choose *New Destination* and specify the following details:


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    User Action
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Name
    
    </td>
    <td valign="top">
    
    Enter a name for the destination.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Description
    
    </td>
    <td valign="top">
    
    Enter a description.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    URL
    
    </td>
    <td valign="top">
    
    `http://<host>:<port>/sap/bc/mcm/json/<repositoryId>`. Here the host and port are the same as configured in cloud connector in the previous steps. The repository ID is the name configured in the section **Connecting the CMIS Repository to the Associated ABAP Connector Class** in [Configuration Settings for SAP Document Management System \(DMS\)](https://help.sap.com/viewer/1317b7d3a93c4763a041b49532666fd7/2021.000/en-US/6ec4f07818b64868bdee115ca83f7109.html).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Proxy Type
    
    </td>
    <td valign="top">
    
    OnPremise
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Authentication
    
    </td>
    <td valign="top">
    
    Enter *BasicAuthentication*.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    User
    
    </td>
    <td valign="top">
    
    Enter your ABAP system user name.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Password
    
    </td>
    <td valign="top">
    
    Enter your ABAP system password.
    
    </td>
    </tr>
    </table>
    
3.  Save your changes.

4.  Choose *Check Connection* to ensure the destination connectivity is available.




<a name="loio6b9df35e0f1e46db8a4abd75d6283937__section_pwx_tzc_jqb"/>

## Onboarding DMS repository Via Document Management Service, Application Option

1.  Navigate to the Admin URL, `https://<your-document_management-endpoint>/admin.html`.

2.  Choose Add *\+* to add the repository.

3.  In the *Add Repository* dialog box, enter the display name and description.

4.  Enter the *Repository ID*. The repository ID is the name configured in the section **Connecting the CMIS Repository to the Associated ABAP Connector Class** in [Configuration Settings for SAP Document Management System \(DMS\)](https://help.sap.com/viewer/1317b7d3a93c4763a041b49532666fd7/2021.000/en-US/6ec4f07818b64868bdee115ca83f7109.html).

5.  Enter the destination name created in the section **Creating a Destination in SAP Business Technology Platform \(SAP BTP\)**.
6.  Choose *Add*. After the DMS repository has been successful onboarded, a message is displayed that the repository has been added.


You can access your repository now at `https://<your-document_management-endpoint>/web.html`.

