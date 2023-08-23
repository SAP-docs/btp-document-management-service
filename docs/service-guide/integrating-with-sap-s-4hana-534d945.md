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
> For this scenario to be successfully implemented, SAP Document Management service, integration option is recommended. There's no support for SAP Document Management service, application option, at this time. SAP S/4 HANA is always be the front end, and we don't support the SAP Document Management service, application option for onboarding the repository, or allowing you to view any files.

For the detailed steps on using document management as a content repository with SAP S/4HANA Cloud, private edition, refer to the [Blog](https://blogs.sap.com/2020/12/31/using-document-management-as-a-content-repository-with-sap-s-4-hana/) post.



### Extend and Integrate Your SAP S/4HANA Cloud

To connect your own CMIS repository to SAP S/4HANA Cloud, public edition, you must follow the configuration steps outlined in this section. See [Integrating SAP Document Management with SAP S/4HANA Cloud.](https://help.sap.com/docs/SAP_S4HANA_CLOUD/0f69f8fb28ac4bf48d2b57b9637e81fa/03414f87d6e14dff9450e20e21632826.html?version=2308.500)

**Related Information**  


[Integrating SAP S/4HANA with Google Workspace Using SAP Document Management Service](integrating-sap-s-4hana-with-google-workspace-using-sap-document-management-service-594bf95.md "Google Workspace includes Google Drive as one of its productivity applications. You can integrate Google Drive as a file share with SAP Document Management Service. Google documents can be opened in a web browser using Google UI. Create, read, update, and delete (CRUD) operations can be performed on your Google documents and folders through this integration.")

[Integrating the ABAP Environment with SAP Document Management Service](integrating-the-abap-environment-with-sap-document-management-service-c54ce8b.md "You can integrate the ABAP environment of SAP Business Technology Platform with SAP Document Management Service to establish a communication scenario.")

