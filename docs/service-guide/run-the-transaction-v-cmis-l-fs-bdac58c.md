<!-- loiobdac58cc00ca4528bba0b520f3785bbc -->

# Run the Transaction V\_CMIS\_L\_FS

Run the transaction to complete the configuration in ABAP on-premise environment



<a name="loiobdac58cc00ca4528bba0b520f3785bbc__prereq_jbl_fcr_5tb"/>

## Prerequisites

You've completed the previous section. For more information, see [Create a Destination in ABAP System Using Transaction SM59](create-a-destination-in-abap-system-using-transaction-sm59-d9e47b5.md).



## Procedure

1.  Open the transaction `V_CMIS_L_FS`.

2.  Enter the *File Share ID* as per your requirements. The name must begin with the letter 'Z'. For example, `ZTEST2`.

3.  In the *File Share* dialog, enter the following details:

    ****


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
    
    Enter your root folder path.
    
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
    

