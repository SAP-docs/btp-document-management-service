<!-- loio65128a9038054fea98e427e753764350 -->

# CAP Plugin

Use SAP Cloud Application Programming Model \(CAP\) Plugin with SAP Document Management Service.

The [cap-js/sdm](https://www.npmjs.com/package/@cap-js/sdm) package operates as a [CDS Plugin](https://cap.cloud.sap/docs/node.js/cds-plugins#cds-plugin-packages), its primary role being the provision of a simplified CAP-level integration route with SAP Document Management Service.

This plugin allows you to store and manage various documents as attachments in a centralized location called the Document Management Repository.

> ### Remember:  
> This plugin is a Node.js plugin and is designed specifically for use with Node.js based applications.



<a name="loio65128a9038054fea98e427e753764350__section_i2h_hs1_wbc"/>

## Plugin Features

-   **Create Attachments:** Easily create new attachments for relevant information sharing.
-   **Delete Attachments:** Simplify your attachments page by removing unnecessary files.
-   **Open and View Attachments:** Directly view attachment content without extra steps.
-   **Rename Attachments:** Keep your files organized and easily identifiable.
-   **Virus Scanning:** When enabled in the repository, all attachments undergo a virus scan before saving. Any document found with a virus is removed.



<a name="loio65128a9038054fea98e427e753764350__section_m35_5vr_5bc"/>

## Prerequisites

The following preparatory steps are required before you start using this plugin:

-   You've subscribed to the service Document Management Service, Integration Option and created an instance in Cloud Foundry environment. See [Initial Setup for Document Management Service, Integration Option](integration-option-guide/initial-setup-for-document-management-service-integration-option-bc0f1ec.md).

-   You've onboarded the repository. For more information about the API for onboarding repositories, see [SAP Business Accelerator Hub](https://api.sap.com/api/AdminAPI/path/post_rest_v2_repositories).
-   You know how to use `cds-plugin` for Node.js. For more information. see [CDS Plugin Packages](https://cap.cloud.sap/docs/plugins/#as-cds-plugins-for-node-js).



<a name="loio65128a9038054fea98e427e753764350__section_pwz_b2s_5bc"/>

## Procedure

1.  Create or use the already existing application to add `Attachments` type to the CDS model.
2.  Follow the detailed step-by-step instructions provided in this [Guide](https://www.npmjs.com/package/@cap-js/sdm).

    > ### Note:  
    > This plugin doesn't support the versioned repositories.


