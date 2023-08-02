<!-- loio66e4071b01be4c02bb3733afb0ffb558 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Configuring User Access

Create roles for the application and assign users to these roles.



## Procedure

1.  Open the SAP BTP cockpit.

2.  Navigate to your subaccount.


Create Roles

3.  In the left pane, choose *Security* \> *Role Collections*.

4.  To create a new role collection, choose :heavy_plus_sign: \(Create New Role Collection\). To copy an existing role collection, choose *Copy* at the end of the row.

5.  Enter a new name and description. If you copied an existing role collection, you can see the included roles.

6.  Add roles to the new role collection by selecting the role name and then choose *Add Role*.

7.  Add roles to the role collection from the following list based on your requirements.


    <table>
    <tr>
    <th valign="top">

    Role


    
    </th>
    <th valign="top">

    Role Capabilities


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *SDM\_Admin* and *SDMWeb\_Admin* 


    
    </td>
    <td valign="top">
    
    Provide admin capabilities to a user. With admin capabilities, a user can add, sync, update, and delete repositories.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *SDM\_User* and *SDMWeb\_User* 


    
    </td>
    <td valign="top">
    
    Provide capabilities to use the web UI of Document Management Service, Application Option.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *SDM\_MigrationAdmin* and *SDMWeb\_Migration* 


    
    </td>
    <td valign="top">
    
    Provide admin capabilities to use the web UI for Document Management Migration. With admin capabilities, you can initiate the migration, check the status, and also download the logs.


    
    </td>
    </tr>
    </table>
    
8.  Choose *Save*.


<a name="task_zwb_yg3_qpb"/>

<!-- task\_zwb\_yg3\_qpb -->

## Assign Users to Role Collections

Assign users to a role collection by adding them to the role collection.



<a name="task_zwb_yg3_qpb__steps_hfp_dh3_qpb"/>

## Procedure

1.  Open the SAP BTP cockpit.

2.  Navigate to your subaccount.

3.  In the left pane, choose *Security* \> *Role Collections*.

4.  Choose the role collection to which you want to assign users.

5.  Go to the *Users* section and choose *Edit*.

6.  Enter the user ID of the user that you want to assign to the role collection. If the user only exists in a connected identity provider, you must choose the identity provider and type in the e-mail address.

7.  **Optional:** To add more users, choose :heavy_plus_sign: \(Add a user\).

8.  Save your changes.

    You've now assigned this user to the role collection. The user has all of the authorizations of the role collection.


