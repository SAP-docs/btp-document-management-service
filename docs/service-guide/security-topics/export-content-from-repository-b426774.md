<!-- loiob4267744c49d4d1baccfc36d36139454 -->

# Export Content from Repository

Use CMIS workbench to export content from your repository.



## Procedure

1.  Download the Chemistry Workbench from the Apache Web site and connect to your repository.

2.  Download the content of your repository to your local computer.

    > ### Note:  
    > To set up automated batch operations, you can use *Console* in the CMIS workbench. You can create scripts that perform queries to filter your content or you can download selective folders only. As starting point, have a look at the sample scripts that are available in the *Console* menu.

    > ### Remember:  
    > -   Repository exports are restricted to a maximum size of 4 GB. Exceeding this 4-GB limit isn't permitted.
    > 
    > -   REST-based APIs now let you off-board your repository as well as check the status of offboarding and download the repository data. Refer to an API published on [SAP Business Accelerator Hub](https://api.sap.com/api/AdminAPI/resource).


<a name="task_isf_wlc_gzb"/>

<!-- task\_isf\_wlc\_gzb -->

## The Alternative Approach to Exporting Content

There are different ways to export content from your repositories, and you can use any of them.



<a name="task_isf_wlc_gzb__context_vfq_nmc_gzb"/>

## Context

This is applicable to Document Management Service, Integration Option. For example, you could use a REST API to export your content.



<a name="task_isf_wlc_gzb__steps_s5y_dmc_gzb"/>

## Procedure

1.  To get started with exporting the content, follow these steps:

    1.  When you're trying to download content from the repositories, you need to execute the API calls one by one in the same order as follows:

        1.  Prepare for content creation using the `ZIP Content Creation` API published on [SAP Business Accelerator Hub](https://api.sap.com/api/ZipCreationForDownload/overview).

        2.  Download content using the `ZIP Content Download` API published on [SAP Business Accelerator Hub](https://api.sap.com/api/GetZipContentStream/overview).



2.  To export the metadata of repositories, use the `Fetch Repository` API published on [SAP Business Accelerator Hub](https://api.sap.com/api/ServiceApi/overview).


