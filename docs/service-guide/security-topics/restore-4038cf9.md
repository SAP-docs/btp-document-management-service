<!-- loio4038cf96fd58486bb39d7e7553823015 -->

# Restore

Document Management Service allows the restoration of content based on the cause of data loss. Restore a deleted repository and instance to a previous state.



## Context

In certain situations, it's necessary to restore repositories and instances that you've accidentally deleted. Submit a service request by opening a support case and provide all of the information required to complete the restoration process. Our internal team carries out the request and update the support case accordingly. Create a new case for each request.

> ### Remember:  
> It's only possible to restore deleted repositories or instances if they're deleted within 14 days after the date of deletion. It's not possible to restore repositories or instances that have been deleted older than 14 days.

You can submit a restoration request by following the procedures:

<a name="task_nkc_kjd_fqb"/>

<!-- task\_nkc\_kjd\_fqb -->

## Restoring a Deleted Repository

You can request the restoration of a deleted repository by following the steps described in this topic.



<a name="task_nkc_kjd_fqb__steps_cym_qjd_fqb"/>

## Procedure

1.  Raise a new support case under the component **BC-CP-CF-SDM-INT**.

2.  In the *Subject* field, begin with the word **Repository Restore**.

3.  In the *Description* field, provide the following information:


    <table>
    <tr>
    <th valign="top">

    Parameter Name


    
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
    
    Service URL.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `ZoneId`


    
    </td>
    <td valign="top">
    
    Include the `zoneId` of the instance.

    > ### Example:  
    > "zoneId":"9e5f9fb4-32bd-479a-a3dd-59a126b9e3ff"


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `SubaccountId`


    
    </td>
    <td valign="top">
    
    Copy ID from the *Subaccount Details* section.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `serviceInstanceId`


    
    </td>
    <td valign="top">
    
    The instance ID of the service instance.


    
    </td>
    </tr>
    </table>
    
4.  Submit the request.

    Your support case is processed further once you submit the request, and you receive an update.


<a name="task_hkc_ckd_fqb"/>

<!-- task\_hkc\_ckd\_fqb -->

## Restoring a Deleted Instance

You can request the restoration of a deleted instance by following the steps described in this topic.



<a name="task_hkc_ckd_fqb__prereq_tkg_nvd_fqb"/>

## Prerequisites

You've created a new service instance. See [Creating a Service Instance and Service Key](../integration-option-guide/creating-a-service-instance-and-service-key-fe7f1e5.md).



<a name="task_hkc_ckd_fqb__context_nkd_dwd_fqb"/>

## Context

Before requesting that a deleted service instance to be restored, you've created a new service instance within the same subaccount. Make sure that the new instance is empty. Because it's not possible to restore a repository to the same instance after it has been deleted. All deleted repositories are migrated to the new instance.



<a name="task_hkc_ckd_fqb__steps_ikc_ckd_fqb"/>

## Procedure

1.  Raise a new support case under the component **BC-CP-CF-SDM-INT**.

2.  In the *Subject* field, begin with the word **Instance Restore**.

3.  In the *Description* field, provide the following information:


    <table>
    <tr>
    <th valign="top">

    Parameter Name


    
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
    
    Service URL.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `SubaccountId`


    
    </td>
    <td valign="top">
    
    Copy ID from the *Subaccount Details* section.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `inactiveServiceInstanceId`


    
    </td>
    <td valign="top">
    
    Include the ID of the deleted service instance.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `activeServiceInstanceId`


    
    </td>
    <td valign="top">
    
    Include the ID of the newly created service instance.


    
    </td>
    </tr>
    </table>
    
4.  Submit the request.

    Your support case is processed further once you submit the request, and you receive an update.


<a name="task_wqh_wjv_5qb"/>

<!-- task\_wqh\_wjv\_5qb -->

## Restoring Because of Technical Problem

If there's a technical failure, the Document Management Service allows you to restore your content. The last restore point provided by underlying storage and hyperscalar can vary depending on the reason of failure.

