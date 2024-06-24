<!-- loio65128a9038054fea98e427e753764350 -->

# CAP Plugin

Use SAP Cloud Application Programming Model \(CAP\) Plugin with SAP Document Management Service.

The [cap-js/sdm](https://github.com/cap-js/sdm) package operates as a [CDS Plugin](https://cap.cloud.sap/docs/node.js/cds-plugins#cds-plugin-packages), its primary role being the provision of a simplified CAP-level integration route with SAP Document Management Service.

This plugin allows you to store and manage various documents as attachments in a centralized location called the Document Management Repository.



<a name="loio65128a9038054fea98e427e753764350__section_m35_5vr_5bc"/>

## Prerequisites

The following preparatory steps are required before you start using this plugin:

-   You've subscribed to the service Document Management Service, Integration Option and created an instance in Cloud Foundry environment. See [Initial Setup for Document Management Service, Integration Option](integration-option-guide/initial-setup-for-document-management-service-integration-option-bc0f1ec.md).

-   You've created a service binding for the consuming application. For more information about service binding, see [Binding Service Instances to Cloud Foundry Applications](https://help.sap.com/docs/service-manager/sap-service-manager/binding-service-instances-to-cloud-foundry-applications?version=Cloud&locale=en-US).
-   You've onboarded the repository. For more information about the API for onboarding repositories, see [SAP Business Accelerator Hub](https://api.sap.com/api/AdminAPI/path/post_rest_v2_repositories).
-   You know how to use `cds-plugin`. For more information. see [CDS Plugin Packages](https://cap.cloud.sap/docs/node.js/cds-plugins#cds-plugin-packages).



<a name="loio65128a9038054fea98e427e753764350__section_pwz_b2s_5bc"/>

## Procedure

1.  Create or use the already existing application to add `Attachments` type to the CDS model.
2.  Follow the detailed step-by-step instructions provided in this [Guide](https://github.com/cap-js/sdm?tab=readme-ov-file#use-sdm).

