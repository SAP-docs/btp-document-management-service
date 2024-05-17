<!-- loioa84e59ada1294aff8acf2bc72f0ff8a3 -->

# Create File Share in ABAP System

Configure the File Shares using the Secure File Share Configuration app to ensure the functionality of the File Share operations.



<a name="loioa84e59ada1294aff8acf2bc72f0ff8a3__section_j45_yxm_cbc"/>

## Prerequisites

Before you get started, verify that your system meets the following prerequisites:

-   You've completed the previous task. For more information, see [Create a Destination in ABAP System Using Transaction SM59](create-a-destination-in-abap-system-using-transaction-sm59-d9e47b5.md).

-   For `SAP_BASIS >= 7.58 SP01`: You've assigned an administrator authorization with the role template `SAP_BC_CMIS_FS_ADMIN (from 7.58 SP01)` and ensure that you've included the authorization `S_FSC_ADM`. For more information, see [SAP Note 3432542 - Template Role For File Share Configuration](https://me.sap.com/notes/3432542/E).




<a name="loioa84e59ada1294aff8acf2bc72f0ff8a3__section_gh5_sym_cbc"/>

## Procedure for SAP\_BASIS <= 7.58 SP00

Run the transaction to complete the configuration in the ABAP on-premise environment.

1.  Open the transaction `V_CMIS_L_FS`.
2.  Enter the *File Share ID* as per your requirements. The name must begin with the letter 'Z'. For example, `ZTEST2`.
3.  In the *File Share* dialog, enter the following details:


    <table>
    <tr>
    <th valign="top">

    Field Name
    
    </th>
    <th valign="top">

    Values
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *File Share Type*
    
    </td>
    <td valign="top">
    
    `Personal`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Server Type*
    
    </td>
    <td valign="top">
    
    `CMIS`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Destination*
    
    </td>
    <td valign="top">
    
    Destination that you created using the transaction SM59. For example, `ZCA325_SAP_COM_0190_0002` 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Repository ID*
    
    </td>
    <td valign="top">
    
    Enter your repository ID. For example, `GOOGLE_DRIVE`.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Root Folder Path*
    
    </td>
    <td valign="top">
    
    It's an optional setting. Leave empty to automatically address the root of the referenced repository. For example: /My Drive.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Description*
    
    </td>
    <td valign="top">
    
    Enter the meaningful description as per your requirement.
    
    </td>
    </tr>
    </table>
    



<a name="loioa84e59ada1294aff8acf2bc72f0ff8a3__section_fml_fzm_cbc"/>

## Procedure for SAP\_BASIS \>= 7.58 SP01

Follow these steps to successfully setup file share.

1.  Log on to the SAP Fiori Launchpad.
2.  Search for the *Manage File Share Configuration* \(previously*: Secure File Share Configuration*\) app from the SAP Fiori Launchpad. Or open transaction `WDA0146`.
3.  Add a new *File Share* configuration and follow the sub-steps:
    1.  Choose *Create new File Share*.
    2.  In the step *Details*, select a unique *ID* and *Description* and set the *Server* and *File Share Type*.
    3.  Next in the step **Connection**, add the *File Share Destination* and if necessary *File Share Administration Destination*, created in the previous section \([Create a Destination in ABAP System Using Transaction SM59](create-a-destination-in-abap-system-using-transaction-sm59-d9e47b5.md)\). Use the *Check Connection* button to confirm the functionality of your destinations.
    4.  In step **Repository**, select the *Repository ID* as created in the SAP Document Management service and its *Root*.
    5.  Check the information in *Summary*, perform checks if needed, and *Finish* the creation.

4.  If the required File Share exists and needs to be changed, go back to the *Manage File Share Configuration* \(previously*: Secure File Share Configuration*\) app and adapt the fields by following the sub-steps:
    1.  Choose *Edit*.
    2.  Change the settings that have to be changed.

        > ### Note:  
        > If the File Share is already actively used, not all fields can be changed anymore.

    3.  Choose *Save*.

5.  Perform tests on field values, connections to destinations, and the File Share using the *Check File Share* option available within the app.
6.  A *File Share*configuration consists of the following information:


    <table>
    <tr>
    <th valign="top">

    Field Name
    
    </th>
    <th valign="top">

    Values
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *File Share ID*
    
    </td>
    <td valign="top">
    
    Unique identifier of the File Share. The ID must begin with the letter 'Z'. For example, `ZTEST2` 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Description*
    
    </td>
    <td valign="top">
    
    Enter the meaningful description as per your requirement.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *File Share Type*
    
    </td>
    <td valign="top">
    
    `Personal`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Server Type*
    
    </td>
    <td valign="top">
    
    `CMIS`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Destination*
    
    </td>
    <td valign="top">
    
    Destination that you created using the transaction SM59. For example, `ZCA000_SAP_COM_0190_0001` 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Administration Destination* 
    
    </td>
    <td valign="top">
    
    Destination that you created using the transaction SM59. This destination is only used for the technical user scenario. For example, `ZCA000_SAP_COM_0191_0001` 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Inbound Destination*
    
    </td>
    <td valign="top">
    
    It is required to enable the exchange between SAP and a remote system of the vendor for events, for example, linking the document. Required is the name of the destination to the ABAP system created in the SAP BTP subaccount. \(Available from 7.58 SP02 or higher\).

    For example, XYZ\_000
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Repository ID*
    
    </td>
    <td valign="top">
    
    Enter your repository ID. For example, `GOOGLE_DRIVE`.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Root Folder Path*
    
    </td>
    <td valign="top">
    
    This is an optional setting. Leave empty to automatically address the root of the referenced repository. For example: /My Drive.
    
    </td>
    </tr>
    </table>
    

