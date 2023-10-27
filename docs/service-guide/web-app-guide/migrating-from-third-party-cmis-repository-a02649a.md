<!-- loioa02649a4837e4c838433ea5c1f144efc -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Migrating from Third-Party CMIS Repository

Migrate third-party CMIS repositories to SAP Document Management Service in the Cloud Foundry environment.



<a name="loioa02649a4837e4c838433ea5c1f144efc__prereq_hgt_vw3_crb"/>

## Prerequisites

You've created HTTP destination and selected the following parameters. For more information, see [Create HTTP Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/783fa1c418a244d0abb5f153e69ca4ce.html).


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

`URL`

</td>
<td valign="top">

The repository's CMIS browser binding URL.

</td>
</tr>
<tr>
<td valign="top">

`User` 

</td>
<td valign="top">

The repository's username.

</td>
</tr>
<tr>
<td valign="top">

`Password` 

</td>
<td valign="top">

For the given username, a password is required.

</td>
</tr>
</table>



## Procedure

1.  Navigate to the *Document Management Migration* view.

2.  Choose :heavy_plus_sign: icon.

3.  In the dialog box that appears, choose *Third Party Repository* option.

4.  Choose *Destination Name* from the drop-down.

5.  In the *Source Repository* section, enter any *Name*.

6.  Enter *Repository ID* that you want to migrate.

7.  Enter *Destination Name* or select from the dropdown.

8.  **Optional:** In the *Target Repository* section, choose the following options:

    -   Versionable

    -   Virus Scan

    -   Encryption

    -   Thumbnail


9.  Choose *Migrate*.

    Wait for the migration to complete. Depending on the size of the repository, migration can take some time. You can see the current status by refreshing the table.


