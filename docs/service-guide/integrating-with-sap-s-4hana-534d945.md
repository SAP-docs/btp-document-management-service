<!-- loio534d945a3c7c4240bea101e33f25f3be -->

# Integrating with SAP S/4HANA

Document Management Service offers both Inbound and Outbound integration with SAP S/4HANA.



## Inbound Scenario

From SAP Document Management Service, it's possible to onboard SAP S/4HANA DMS as an external repository and browse its contents. The following capabilities are enabled from SAP document management service with SAP S/4HANA DMS repositories:

-   Document management features including the ability to create, edit, and delete documents or folders.

-   Creating Links

-   Basic search and metadata search

-   Rendition viewer

-   Status management

-   Classification

> ### Note:  
> The integration is only supported with SAP S/4HANA DMS on-premise and not with the cloud version. For the detailed steps on onboarding DMS repositories, refer to the [Blog](https://blogs.sap.com/2020/08/14/connect-sap-document-management-application-option-to-dms/) post.



<a name="loio534d945a3c7c4240bea101e33f25f3be__section_w11_cfz_jrb"/>

## Outbound Scenario

SAP Document Management service, integration option can be used as a content server from SAP S/4HANA attachment service.

The Document Management Service, Integration Option enables you to onboard any CMIS-compliant repository to be used as a content server.

> ### Caution:  
> For this scenario to be successfully implemented, SAP Document Management service, integration option is recommended. There is no support for SAP Document Management service, application option, at this time. SAP S/4 HANA will always be the front end, and we do not support the SAP Document Management service, application option for onboarding the repository, or allowing you to view any files.

For the detailed steps on using document management as a content repository with SAP S/4HANA, refer to the [Blog](https://blogs.sap.com/2020/12/31/using-document-management-as-a-content-repository-with-sap-s-4-hana/) post.

**Related Information**  


[Integrating SAP S/4HANA with Google Workspace Using SAP Document Management Service](integrating-sap-s-4hana-with-google-workspace-using-sap-document-management-service-594bf95.md "Google Workspace includes Google Drive as one of its productivity applications. You can integrate Google Drive as a file share with SAP Document Management Service. Google documents can be opened in a web browser using Google UI. Create, read, update, and delete (CRUD) operations can be performed on your Google documents and folders through this integration.")

[Integrating the ABAP Environment with SAP Document Management Service](integrating-the-abap-environment-with-sap-document-management-service-c54ce8b.md "You can integrate the ABAP environment of SAP Business Technology Platform with SAP Document Management Service to establish a communication scenario.")

