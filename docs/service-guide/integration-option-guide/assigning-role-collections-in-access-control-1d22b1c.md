<!-- loio1d22b1c4d9054bceb6073ef08145db1b -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Assigning Role Collections in Access Control

As an administrator, when you want to assign role collections for the documents and folders, you create a role collection and assign it in the *Access Control* list of your documents and folders.



<a name="loio1d22b1c4d9054bceb6073ef08145db1b__prereq_pq4_z5v_s4b"/>

## Prerequisites

-   You've created a role collection from your subaccount of SAP BTP Cockpit and assigned users in it. For more information, see [Define a Role Collection](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/4b20383efab341f181becf0a947a5498.html) and [Assign Users to Role Collections](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/c5766765bda74ad59fe656977c8fa4d6.html).

-   You've created an internal repository. For more information, see [Onboarding Internal Repository](../web-app-guide/onboarding-internal-repository-59e3cb7.md).




## Context

Role collections are sets of authorizations that are suitable for distinct user groups. You want to assign these role collections to your documents and folders.



## Procedure

1.  Open an internal repository and choose <span class="SAP-icons-V5"></span> More Options.

2.  Choose *Show Properties* \> *Edit* \> *Access Control*.

3.  Enter the principals to add a role collection in the following format and choose *Add*.

    Add a prefix `~group~` as it's before the *Role Collection* that you configured in SAP BTP Cockpit.

    > ### Example:  
    > If you've created a role collection as `HiringManagers` and you need to add group principal in the *Access Control*, then add it in the format `~group~HiringManagers`.

    > ### Remember:  
    > -   If you want to add Access Control principals with email and group name, you can separate it out using a semicolon \(;\). For example, in the following principal semicolon \(;\) has been used as a delimiter when adding access control principals.
    > 
    >     ```
    >     test@sap.com;~group~HiringManagers
    >     ```
    > 
    > -   If you want to include multiple principals, then the delimiter semicolon \(;\) is used in the following format. Spaces are also supported in group names.
    > 
    >     -   Group name without space:
    > 
    >         ```
    >         abc@sap.com;xyz@sap.com;~group~HiringManagers
    >         ```
    > 
    >     -   Group name with Space:
    > 
    >         ```
    >         abc@sap.com;~group~Hiring Managers
    >         ```
    > 
    > 
    > -   White spaces in the role collection are supported. When there is only one group name with a space, the delimiter semicolon \(;\) must be used at the end of the principal.
    > 
    >     > ### Example:  
    >     > ```
    >     > ~group~Hiring Managers;
    >     > ```
    > 
    > -   When adding a principal to a role collection, don't duplicate the principal ID.

4.  In the *Permission* list, pick the access that you want to provide.

5.  Choose *Save*.


