<!-- loio87e11986ee8040d78872393c54c5f950 -->

# Maintain HTTP Allowlist in SAP S/4HANA \(On Premise\)

Configure HTTP context types in SAP S/4HANA\(On Premise\) to manage HTTP allowlist.



## Procedure

1.  Log on to your SAP S/4HANA system as administrator.

2.  Start the transaction `UCONCOCKPIT` \(Unified Connectivity\).

3.  Choose the *HTTP Allowlist* scenario.

4.  Set up the check modes for the *Trusted Network Zone* HTTP context type. Use the following details to maintain HTTP allowlist checks:


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
    
    *Scheme*


    
    </td>
    <td valign="top">
    
    `HTTPS`


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Host*


    
    </td>
    <td valign="top">
    
    `docs.google.com`


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Port*


    
    </td>
    <td valign="top">
    
    `443`


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Path*


    
    </td>
    <td valign="top">
    
    `Maintain Google Doc Path`


    
    </td>
    </tr>
    </table>
    
    For more information about HTTP allowlist, see [Unified Connectivity](https://help.sap.com/docs/ABAP_PLATFORM_NEW/1ca554ffe75a4d44a7bb882b5454236f/ad6340c911164f639877e2dfb51d4b49.html?locale=en-US&version=201909.001).


