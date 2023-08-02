<!-- loio48f6f9d8485f4b3b9d8304ed37ff8f34 -->

# Migrating Application to SAP Document Management Service from Neo Environment

Use this procedure if you're planning to migrate application from Neo to Cloud Foundry environment.



<a name="loio48f6f9d8485f4b3b9d8304ed37ff8f34__prereq_rl3_nrb_hpb"/>

## Prerequisites

-   You've subscribed to the service Document Management Service, Integration Option and created an instance in Cloud Foundry environment. See [Initial Setup for Document Management Service, Integration Option](../integration-option-guide/initial-setup-for-document-management-service-integration-option-bc0f1ec.md).

-   You've copied the `clientid`, `clientsecret`, and `tokenurl` parameters generated in the same subaccount of Cloud Foundry environment where Document Management, integration option instance is created. For more information about creating parameters, see [Create Service Keys Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cdf4f200db3e4c248fa67401937b2f78.html).

-   You've generated the bearer token from the client credentials in theSAP Document Management Service. See [Generate a JSON Web Token](../integration-option-guide/generate-a-json-web-token-bff9fd6.md).

-   The global administrator of your SAP BTP account has added the service plan for Document Management Service, Repository Option to your subaccount via entitlements. See [Configure Entitlements for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).

-   You've onboarded Document Management provided storage capability. See [Connecting to Document Management Service, Repository Option Using API](../integration-option-guide/connecting-to-document-management-service-repository-option-using-api-d30200e.md).




## Context

As all of the capabilities and functionalities are the same as in the Neo environment, you don't need to modify any logical code in your application. The only place you need to change the application code is where you're creating a CMIS session. Both solutions are CMIS-compliant, and you can use the APIS to bind to any CMIS-based repository.



## Procedure

1.  In your `pom.xml` file of Java project, add the following dependencies.

    > ### Sample Code:  
    > ```
    > 
    > 		<dependency>
    > 		  <groupId>org.apache.chemistry.opencmis</groupId>
    > 		  <artifactId>chemistry-opencmis-client-impl</artifactId>
    > 		  <version>1.1.0</version>
    > 		</dependency>
    > 		 
    > 		<dependency>
    > 		  <groupId>org.apache.chemistry.opencmis</groupId>
    > 		  <artifactId>chemistry-opencmis-client-api</artifactId>
    >   		<version>1.1.0</version>
    > 		</dependency>
    > 
    > ```

2.  Prepare the session parameters in the same way that they were in the Neo environment, with a small change to accommodate the OAuth token and the service url in the session map. After you've enhanced the session parameters, the map content could look something like the following:

    > ### Sample Code:  
    > ```
    > 		
    > 		org.apache.chemistry.opencmis.binding.spi.type=browser
    > 		org.apache.chemistry.opencmis.binding.browser.url=https://<service-URL>/browser
    > 		org.apache.chemistry.opencmis.oauth.accessToken=eyJhbGciOi..<Your Token>
    > 		org.apache.chemistry.opencmis.session.repository.id=<repository_id>
    > 		org.apache.chemistry.opencmis.binding.auth.http.basic=false
    > 		org.apache.chemistry.opencmis.binding.auth.soap.usernametoken=false
    > 		org.apache.chemistry.opencmis.binding.auth.http.oauth.bearer=true
    > 		org.apache.chemistry.opencmis.binding.useragent=OpenCMIS-Workbench/1.1.0-sap-03 Apache-Chemistry-OpenCMIS/1.1.0-sap-03 (Java 1.8.0_281; Windows 10 10.0)
    > 		org.apache.chemistry.opencmis.binding.compression=true
    > 		org.apache.chemistry.opencmis.binding.clientcompression=false
    > 		org.apache.chemistry.opencmis.binding.cookies=true
    > 		org.apache.chemistry.opencmis.locale.iso639=en
    > 		org.apache.chemistry.opencmis.binding.connecttimeout=30000
    > 		org.apache.chemistry.opencmis.binding.readtimeout=600000
    > 
    > ```

    > ### Remember:  
    > When obtaining a session from the Neo environment, it was as follows:
    > 
    > > ### Sample Code:  
    > > ```
    > > EcmFactory.connectForUser(repository.getUniqueName(), repositoryKey, destination, logonId, ecmSessionParameters, groups);
    > > ```
    > 
    > This is a line of code that isn't available in the Cloud Foundry environment, and you must modify it to obtain a session.

3.  Now, if you want to build a CMIS session in the Cloud Foundry environment, you need to use the two CMIS classes, and your code should look like the following sample. And you need to pass the parameter map that you created in the previous step.

    > ### Sample Code:  
    > ```
    > 
    > import org.apache.chemistry.opencmis.client.api.Session;
    > import org.apache.chemistry.opencmis.client.api.SessionFactory;
    > import org.apache.chemistry.opencmis.client.runtime.SessionFactoryImpl;
    > 	 
    > SessionFactory sessionFactory = SessionFactoryImpl.newInstance();
    > Session cmisSession = sessionFactory.createSession(<parameterMap>);
    > 
    > ```

    > ### Note:  
    > In the Cloud Foundry environment, don't include or bundle the NEO platform or SDK-related Jars.


