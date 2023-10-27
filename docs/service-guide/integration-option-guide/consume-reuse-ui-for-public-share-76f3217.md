<!-- loio76f3217944ec4ee9b9e9987794d6136b -->

# Consume Reuse UI for Public Share

Embed the reusable UI component in your SAP Fiori application to display a list of documents from a repository and add document management capabilities for public share.



<a name="loio76f3217944ec4ee9b9e9987794d6136b__prereq_khs_twv_slb"/>

## Prerequisites

-   You’re subscribed to the SAP BTP service *Authorization and Trust Management* to authenticate the users.

-   You’re subscribed to the SAP BTP service *HTML5 Application Repository* to consume Document Management Service's reuse UI.

-   You've created an SAP Fiori application. See [Develop an SAP Fiori Application](https://help.sap.com/viewer/9d1db9835307451daa8c930fbd9ab264/Cloud/en-US/61c7416594984034a5676e63a6494ba1.html).

-   You've onboarded a repository to store your files and folders. See [Manage Document Management Service, Integration Option](manage-document-management-service-integration-option-64fa80a.md).




<a name="loio76f3217944ec4ee9b9e9987794d6136b__context_mxk_4xh_znb"/>

## Context

Document Management Service, Integration Option's reuse UI is a ready-to-use, document management UI that can be easily integrated into any SAP Fiori application. The reuse UI is a UI5 component that enables common document management operations like creating, deleting of folders and documents, updating properties, managing versions, and manage public sharing of resources.



<a name="loio76f3217944ec4ee9b9e9987794d6136b__steps_nxk_4xh_znb"/>

## Procedure

1.  Edit the `mta.yaml` file of your SAP Fiori application.

    1.  Add Document Management Service, Integration Option component under `resources` and add the same as a requirement for the `approuter.nodejs` module.

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
        >       service: sdm
        >       service-plan: standard   	
        > ...
        > 
        > 
        > ```

    2.  For the `approuter.nodejs` module, under the `properties` section, add a destination configuration.

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


2.  Edit the `xs-app.json` file of your SAP Fiori application.

    1.  To route the API calls to Document Management Service, Integration Option's server, add a route to `/public`.

        > ### Sample Code:  
        > ```
        > 
        > 
        > {
        >   routes: [
        >     ...
        >     {
        >       "source": "^/public/(.*)$",
        >       "target": "/public/$1",
        >       "authenticationType": "none",
        >       "destination": "sdibackend",
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
    >           // Optionally pass the settings here or do it in controller with 'setSettings' method
    >           "destinationPath": "/public",
    >           "repositoryId": " ",
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

    To further configure the reuse UI – like using publinkId, destianation path etc., see the following topic *Configurations for Reuse UI in Public Share* .

4.  Add the component to your application, in any view, by defining a `ComponentContainer` and its `usage`.

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


<a name="task_t22_dzh_znb"/>

<!-- task\_t22\_dzh\_znb -->

## Configurations for Reuse UI in Public Share

Learn about the properties of the reuse UI for public share and make configuration changes as per your requirements.



<a name="task_t22_dzh_znb__context_jw5_fzh_znb"/>

## Context

Add the properties while you declare the `componentUsage` to configure the reuse UI for public share in the document management.


<table>
<tr>
<th valign="top">

Name

</th>
<th valign="top">

Required

</th>
<th valign="top">

Type

</th>
<th valign="top">

Default Value

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

`repositoryId` 

</td>
<td valign="top">

Optional

</td>
<td valign="top">

string

</td>
<td valign="top">

empty

</td>
<td valign="top">

The ID of the repository that you want to connect.

</td>
</tr>
<tr>
<td valign="top">

`objectId` 

</td>
<td valign="top">

Yes

</td>
<td valign="top">

string

</td>
<td valign="top">

empty

</td>
<td valign="top">

The ID of the object \(folder/document\) that you want to load.

</td>
</tr>
<tr>
<td valign="top">

`destinationPath` 

</td>
<td valign="top">

Yes

</td>
<td valign="top">

string

</td>
<td valign="top">

`/public`

</td>
<td valign="top">

The path where Document Management, integration option's API is exposed; the path used in the approuter to route request to 'com.sap.ecm.reuse' service.

</td>
</tr>
<tr>
<td valign="top">

`pubLinkId` 

</td>
<td valign="top">

Yes

</td>
<td valign="top">

string

</td>
<td valign="top">

empty

</td>
<td valign="top">

The ID of the public link \(folder/document\) that you want to load.

</td>
</tr>
</table>

> ### Note:  
> Once the public share is made available, you can get the `objectId` and `publinkId`.

