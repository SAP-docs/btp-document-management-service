<!-- loio21bd2788d7c74c43a399dc13cf452f0c -->

# Connecting Your Own Repository to Document Management Service, Integration Option

Connect your choice of CMIS-compliant, on-premise, or cloud repository to Document Management Service, Integration Option using REST APIs.



<a name="loio21bd2788d7c74c43a399dc13cf452f0c__prereq_bzc_h1w_clb"/>

## Prerequisites

-   You’ve connected your on-premise repository to SAP BTP using a Cloud Connector. For more information, see [Cloud Connector](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/e6c7616abb5710148cfcf3e75d96d596.html).

-   You’ve configured a destination for your repository in SAP BTP cockpit to connect to Document Management Service. For more information, see [HTTP Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/42a0e6b966924f2e902090bdf435e1b2.html).

-   You've completed one of these tasks:

    -   [Bind Service Instances to Applications Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/2d2a3e8b2f1348ffbb54eaae10d80b95.html)

    -   [Create Service Keys Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cdf4f200db3e4c248fa67401937b2f78.html).


-   You've the `SDM_Admin` scope to execute the admin APIs.




## Context

To add your repository using a REST API, you must generate a JSON Web Token \(JWT\). Use the JWT as your authorization to make the onboarding REST API callls. For more information, see [SAP Business Accelerator Hub](https://api.sap.com/api/AdminAPI/resource).

-   [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)

-   [Add Your Repository Using the Onboarding API](add-your-repository-using-the-onboarding-api-5fccabb.md)


If you would like to use SAP's storage, see [Connecting to Document Management Service, Repository Option Using API](connecting-to-document-management-service-repository-option-using-api-d30200e.md).

