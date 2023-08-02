<!-- loio00af52a4449b469c8b548723589aba0b -->

# Consume Reuse UI for Admin Option

Embed the reusable UI for admin component in your SAP Fiori application to display a list of documents from a repository and add document management capabilities.



<a name="loio00af52a4449b469c8b548723589aba0b__prereq_khs_twv_slb"/>

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


2.  Edit the `xs-app.json` file in the `approuter` module of your SAP Fiori application.

    1.  To route the API calls to Document Management Service, Integration Option's server, add a route to `/api`.

        > ### Sample Code:  
        > ```json
        > 
        > 
        > {
        > 	...
        >   "routes": [
        >     {
        >       "source": "^/api(.*)$",
        >       "target": "$1",
        >       "authenticationType": "xsuaa",
        >       "service": "com.sap.ecm.reuse",
        >       "endpoint": "ecmservice"
        >     },
        >     {
        >       "source": "^(.*)$",
        >       "target": "$1",
        >       "service": "html5-apps-repo-rt",
        >       "authenticationType": "xsuaa"
        >     }
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
    >       "admin": {
    >         "name": "com.sap.ecm.reuse.admin",
    >         "settings": {
    >           "destinationPath": "/api"
    > 
    >           }
    >         }
    >       },
    >      "resourceRoots": {
    >        "com.sap.ecm.reuse.admin": "./../comsapecmreuse.comsapecmreuseadmin/"
    >      },
    >    }
    >   ...
    > }
    > 
    > 
    > ```

    To further configure the reuse UI – like sorting, setting a different home folder, see [Configurations for Reuse UI](configurations-for-reuse-ui-c91ec16.md).

4.  Configure *View* and *Controller* by executing the following option:

    -   Add the component to your application, in any view, by defining a `ComponentContainer` and its `usage`.

        > ### Sample Code:  
        > ```
        > 
        > 
        > <mvc:View controllerName="com.sample.controller.View1" xmlns:core="sap.ui.core" xmlns:mvc="sap.ui.core.mvc" displayBlock="true" xmlns="sap.m">
        > ...
        > <Page id="page" title="{i18n>title}">
        > <content>
        > <core:ComponentContainer usage="admin" height="100%" width="100%" async="false" manifest="true"/>
        > </content>
        > </Page>
        > ...
        > </mvc:View>
        > 
        > 
        > ```



**Related Information**  


[Reuse UI](reuse-ui-c41e52e.md "")

