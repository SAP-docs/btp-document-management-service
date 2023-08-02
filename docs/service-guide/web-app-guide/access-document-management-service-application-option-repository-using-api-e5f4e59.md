<!-- loioe5f4e592f37748759ecd551f3afcd364 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Access Document Management Service, Application Option Repository Using API

You can access repositories onboarded via Document Management Service, Application Option through API by connecting to the instance of Document Management Service, Integration Option.



<a name="loioe5f4e592f37748759ecd551f3afcd364__prereq_yqg_tty_j4b"/>

## Prerequisites

-   You've subscribed to the Document Management Service, Application Option.

    For more information, see [Subscribing to Document Management Service, Application Option](subscribing-to-document-management-service-application-option-cce24e2.md).

-   You've added entitlements for Document Management Service, Integration Option.

    For more information about entitlements, see [Configure Entitlements and Quotas for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).




## Procedure

1.  Create a *Service Instance* and *Service Key* for Document Management Service, Integration Option. For more information, see [Creating a Service Instance and Service Key](../integration-option-guide/creating-a-service-instance-and-service-key-fe7f1e5.md).

2.  In the SAP BTP cockpit, choose *Connectivity* \> *Destinations* \> *New Destination* \> *Service Instance*.

3.  Select the *Service Instance* that you created in the drop-down list.

4.  Enter the *Name* and *Description*.

5.  Choose *Next* \> *Save*.

6.  Open the Document Management Service admin view.

7.  Choose the :pencil2: icon to edit your repository.

8.  In the dialog box that appears, enter the destination name that you created in the field `Service Instance Destination`.

9.  Choose *Save* to update your repository.

10. Consume API to connect your repository. For more information, see [Connecting Your Own Repository to Document Management Service, Integration Option](../integration-option-guide/connecting-your-own-repository-to-document-management-service-integration-option-21bd278.md).

    > ### Remember:  
    > Be familiar with the following:
    > 
    > -   Using Document Management Service, Application Option, it’s mandatory to add a repository and connect it to the Document Management Service, Integration Option to access it via both application and integration.
    > 
    > -   Repositories in Document Management Service, Application Option not connected to the Document Management Service, Integration Option instance, can’t be accessed via the API.
    > 
    > -   Directly onboarded repositories via the Document Management Service, Integration Option instance can't be accessed via the Document Management Service, Application Option UI.


