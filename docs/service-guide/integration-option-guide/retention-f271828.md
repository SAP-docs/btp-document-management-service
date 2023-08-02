<!-- loiof2718288fbc34a39aae660877514819f -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Retention

Use the retention feature of Document Management Service, Application Option to prevent documents from being deleted or modified.



<a name="loiof2718288fbc34a39aae660877514819f__prereq_zz4_fdh_bsb"/>

## Prerequisites

You've provided the `sdmbusinessadmin` role. For more information, see [Authorizations](authorizations-669d25c.md).



## Context

A Retention is the period of time during which a document is deleted. A retention policy is currently in place for documents only. Retention is available at header of managing documents menu.

> ### Remember:  
> -   The *Retention* setting can only be applied to documents, not folders.
> 
> -   Upon setting *Retention*, the property attributes of a particular document cannot be modified.
> 
> -   It's mandatory to set the *Expiration Date* if you want to apply retention.
> 
> -   The *Destruction Date* must be greater than or equal to the *Expiration Date*, it can't be less than the *Expiration Date*.
> 
> -   When a *Destruction Date* and *Expiration Date* are set, they can't be removed or preponed. They can only be postponed until a future date.
> 
> -   The *Expiration Date* and *Destruction Date* must be greater than the current timestamp, so it can't be in the past.
> 
> -   It's mandatory to set the *Expiration Date* when you set destruction.



<a name="loiof2718288fbc34a39aae660877514819f__steps_wby_zfx_zrb"/>

## Procedure

1.  Open any repository.

2.  Choose the <span class="SAP-icons"></span> icon for the document that you want to set the retention.

3.  Choose the *Retention* tab and select *Edit*.

4.  Select *Set Retention* option and follow the substeps:

    1.  In the *Destruction Date* field, provide the date when the destruction process can be triggered.

    2.  In the *Expiration Date* field, provide the date until when you need to preserve the document.

    3.  In the *Start of Retention* field, provide the date from which the retention time has been calculated.


5.  Choose *Save*.


