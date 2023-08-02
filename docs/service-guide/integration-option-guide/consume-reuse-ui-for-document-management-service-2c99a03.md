<!-- loio2c99a03a2b7e42d5be44a7ef07c5f917 -->

# Consume Reuse UI for Document Management Service

Embed the reusable UI component in your SAP Fiori application to display a list of documents from a repository and add document management capabilities.



<a name="loio2c99a03a2b7e42d5be44a7ef07c5f917__prereq_khs_twv_slb"/>

## Prerequisites

-   You’re subscribed to the SAP BTP service **Authorization and Trust Management** to authenticate the users.

-   You’re subscribed to the SAP BTP service **HTML5 Application Repository** to consume Document Management Service's reuse UI.

-   You've created an SAP Fiori application. See [Develop an SAP Fiori Application](https://help.sap.com/viewer/9d1db9835307451daa8c930fbd9ab264/Cloud/en-US/61c7416594984034a5676e63a6494ba1.html).

-   You've onboarded a repository to store your files and folders. See [Manage Document Management Service, Integration Option](manage-document-management-service-integration-option-64fa80a.md).




## Context

Document Management Service, Integration Option's reuse UI is a ready-to-use, document management UI that can be easily integrated into any SAP Fiori application. The reuse UI is a UI5 component that enables common document management operations like creating, deleting of folders and documents, updating properties, managing versions.



## Procedure

1.  Edit the `mta.yaml` file of your SAP Fiori application.

    1.  Add Document Management Service, Integration Option Component under `resources` and add the same as a requirement for the `approuter.nodejs` module.

        > ### Sample Code:  
        > ```
        > 
        > 
        > ...
        > modules:
        >   - name: <approutername>
        >     type: approuter.nodejs
        >     ...
        >     requires:
        >       - name: sdm-instance
        > ...
        > resources:
        > 	- name: sdm-instance
        > 	  type: org.cloudfoundry.managed-service
        > 	  parameters:
        >          service: sdm
        >          service-plan: standard   	
        > ...
        > 
        > 
        > ```

    2.  For the `approuter.nodejs` module, under the `properties` section, add a destination configuration.

        > ### Remember:  
        > You need to change the `url` in the destination to your *ecmservice* url.

        The step is required only if you need integration with Microsoft Office. By adding the destination configuration, you can directly view and edit the MS Office files in the respective MS Office applications.

        > ### Sample Code:  
        > ```
        > 
        > 
        > ...
        > modules:
        >   - name: <approutername>
        >     type: approuter.nodejs
        >     ...
        >     requires:
        >       - name: sdm-instance
        > 	...
        > 	properties:
        >         destinations: "[{\"name\": \"sdibackend\", \"url\": \"https://api-sdm-di.cfapps.sap.hana.ondemand.com\", \"forwardAuthToken\": true}]"
        > ...
        > 
        > 
        > ```


2.  Edit the `xs-app.json` file in the `UI` module of your SAP Fiori application.

    1.  To route the API calls to Document Management Service, Integration Option's server, add a route to `/api`.

        > ### Sample Code:  
        > ```
        > 
        > 
        > {
        >   routes: [
        >     ...
        >     {
        >       "source": "^/api/(.*)$",
        >       "target": "$1",
        >       "authenticationType": "xsuaa",
        >       "service": "com.sap.ecm.reuse",
        >       "endpoint": "ecmservice"
        >     },
        >     ...
        >   ]
        > }
        > 
        > 
        > ```


3.  To use Document Management Service, Integration Option's reuse UI as a component in your application, declare a `componentUsage` in the `manifest.json` file of your SAP Fiori applications. Also, declare a `resourceRoots` to point to the HTML5 repository path that contains the reuse UI.

    > ### Sample Code:  
    > ```
    > 
    > 
    > {
    >   ...
    >   "sap.ui5": {
    >     ...
    >     "componentUsages": {
    >       "documentTable": {
    >         "name": "com.sap.ecm.reuse.documentTable",
    >         "settings": {
    >           "repositoryId": "<REPOSITORY_ID>",
    >           "objectId": "<FOLDER_ID>",
    >           }
    >         }
    >       },
    >      "resourceRoots": {
    >        "com.sap.ecm.reuse.documentTable": "./../comsapecmreuse.comsapecmreusedocumentTable/"
    >      },
    >    }
    >   ...
    > }
    > 
    > 
    > ```

    To further configure the reuse UI – like sorting, setting a different home folder, see [Configurations for Reuse UI](configurations-for-reuse-ui-c91ec16.md).

4.  Configure *View* and *Controller* by executing one of the following options :

    -   Add the component to your application, in any view, by defining a `ComponentContainer` and its `usage`.

        > ### Sample Code:  
        > ```
        > 
        > 
        > <mvc:View controllerName="com.sample.controller.View1" xmlns:core="sap.ui.core" xmlns:mvc="sap.ui.core.mvc" displayBlock="true" xmlns="sap.m">
        > ...
        > <Page id="page" title="{i18n>title}">
        > <content>
        > <core:ComponentContainer usage="documentTable" height="100%" async="false" manifest="true"/>
        > </content>
        > </Page>
        > ...
        > </mvc:View>
        > 
        > 
        > ```

    -   Implement the event handler for `componentCreate` event and use the *ReuseUI* component to request navigation to repositories or folders during runtime. Set a home folder.

        > ### Sample Code:  
        > ```
        > 
        > sap.ui.define(["sap/ui/core/mvc/Controller"], function(Controller) {
        >   "use strict";
        >   return Controller.extend("com.sap.sample.sdm", {
        >     onInit: function () {
        >       // OPTIONAL: pass the same settings here, if not added in 'manifest.json' as per previous steps
        >       this.getView().byId("sdi-container").setSettings({
        >         "repositoryId": <REPOSITORY_ID>,
        >         "objectId": <OBJECT_ID>,
        >         "forceLoad": false
        >       });
        >     },
        >     // registered event handler for 'componentCreated' event of Component Container
        >     onComponentCreated: function(oEvent) {
        >       this._oDocumentTable = oEvent.getParameter("component");
        >       // OPTIONAL: set a folder as home folder
        >       this._oDocumentTable.setHomeFolder(<OBJECT_ID>);
        >       // OPTIONAL: request a navigation to a repository & folder during runtime
        >       this._oDocumentTable.requestNavigationAndOpen(<REPOSITORY_ID>, <OBJECT_ID>);
        >     },
        >   });
        > });
        > 
        > ```


    > ### Tip:  
    > For scenario-specific details, refer to the blog post [Consumption of Reuse UI from SAP Document Management Service in SAP Fiori Application](https://blogs.sap.com/2021/04/08/consumption-of-reuse-ui-from-sap-document-management-service-in-sap-fiori-application/).


**Related Information**  


[Reuse UI](reuse-ui-c41e52e.md "")

