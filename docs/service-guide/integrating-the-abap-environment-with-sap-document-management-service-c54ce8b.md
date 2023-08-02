<!-- loioc54ce8bf037142f39e6a7b73b992c519 -->

# Integrating the ABAP Environment with SAP Document Management Service

You can integrate the ABAP environment of SAP Business Technology Platform with SAP Document Management Service to establish a communication scenario.



<a name="loioc54ce8bf037142f39e6a7b73b992c519__prereq_hwv_vvj_jpb"/>

## Prerequisites

-   You've subscribed to the service Document Management Service, Integration Option and created an instance in Cloud Foundry environment. See [Initial Setup for Document Management Service, Integration Option](integration-option-guide/initial-setup-for-document-management-service-integration-option-bc0f1ec.md).

-   The global administrator of your SAP BTP account has added the service plan for Document Management Service, Repository Option to your subaccount via entitlements. See [Configure Entitlements for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).

-   You've onboarded Document Management provided storage capability. See [Connecting to Document Management Service, Repository Option Using API](integration-option-guide/connecting-to-document-management-service-repository-option-using-api-d30200e.md).

-   You've created and copied the service key in the same subaccount of Cloud Foundry environment where Document Management, integration option instance is created. For more information about creating service key, see [Create Service Keys Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cdf4f200db3e4c248fa67401937b2f78.html).

-   You've the *Administrator* role \(role template `ID SAP_BR_ADMINISTRATOR`\). See [Maintain Business Roles](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8980ad05330b4585ab96a8e09cef4688.html).



## Context

SAP Document Management Service assists companies with managing records or attachments that are linked to business objects or a specific business context.

For each tenant of SAP BTP ABAP environment, a service instance of SAP Document Management Service in Cloud Foundry environment has to be created.

You can build and edit communication arrangements that your organization has set up with a communication partner using the *Communication Arrangement* application. The system provides communication scenarios for inbound and outbound communication that you can use to create communication arrangements. Inbound communication describes how a communication partner receives business documents, while outbound communication describes how a communication partner sends business documents to a communication partner. The communication scenario specifies the authorizations, inbound and outbound services, and supported authentication methods that are necessary for the communication.

**Related Information**  


[Integrating with SAP S/4HANA](integrating-with-sap-s-4hana-534d945.md "Document Management Service offers both Inbound and Outbound integration with SAP S/4HANA.")

[Integrating SAP S/4HANA with Google Workspace Using SAP Document Management Service](integrating-sap-s-4hana-with-google-workspace-using-sap-document-management-service-594bf95.md "Google Workspace includes Google Drive as one of its productivity applications. You can integrate Google Drive as a file share with SAP Document Management Service. Google documents can be opened in a web browser using Google UI. Create, read, update, and delete (CRUD) operations can be performed on your Google documents and folders through this integration.")

[Create a Communication Arrangement](create-a-communication-arrangement-7ed34e1.md "Create a communication arrangement in the ABAP environment.")

