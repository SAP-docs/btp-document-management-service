<!-- loio207c51e26fcf430eb7c3f46d335eab3b -->

# Creating Inbound HTTP Destination

Create a destination in your SAP BTP subaccount to connect SAP BTP with SAP S/4HANA Cloud.



<a name="loio207c51e26fcf430eb7c3f46d335eab3b__prereq_mtb_2ds_nbc"/>

## Prerequisites

-   You have administrator privileges for your SAP BTP subaccount.

-   You have already created a Communication Arrangement. For more information, see [Setting Up Inbound Configuration Between SAP BTP and SAP S/4HANA Cloud](setting-up-inbound-configuration-between-sap-btp-and-sap-s-4hana-cloud-5aa38f2.md).



## Procedure

1.  In your subaccount, go to the left navigation pane and choose *Connectivity* \> *Destinations*.

2.  Choose *New Destination*.

3.  In the *Destination Configuration* section, provide values in the following fields:


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
    
    Optional: Provide a description for your reference.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *URL*
    
    </td>
    <td valign="top">
    
    Fill in the URL of your SAP S/4HANA Cloud system.

    Add the following path to the URL: `/sap/opu/odata4/sap/fsitem_noti_eve_api/srvd_a2x/sap/fsitem_noti_eve/0001/NotificationEvent`
    
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
    
    BasicAuthentication
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *User*
    
    </td>
    <td valign="top">
    
    User name that was created as part of the Inbound Communication System configuration.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Password*
    
    </td>
    <td valign="top">
    
    Password that was specified as part of the Inbound Communication System configuration.
    
    </td>
    </tr>
    </table>
    

