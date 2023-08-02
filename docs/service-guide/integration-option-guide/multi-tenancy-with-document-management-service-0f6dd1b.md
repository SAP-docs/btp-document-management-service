<!-- loio0f6dd1bbaca342ee9177b9ece3fcaaa3 -->

# Multi-Tenancy with Document Management Service

Document Management Service is a multi-tenant application, which means that all users have access to the similar components.

SAP Document Management Service can help leading application to build multitenant applications. With Document Management Service, leading applications can choose from Document Management Service managed multi-tenancy and application-managed multi-tenancy as per your requirements.



<a name="loio0f6dd1bbaca342ee9177b9ece3fcaaa3__section_tgs_lfk_jrb"/>

## Multi-tenancy Managed by Document Management Service

-   The Document Management Service handles multi-tenancy.

-   A repository is created in the tenant, which generates the JWT token.

-   The repository of one tenant can't be accessed by another tenant.

-   Either through reuse service or token exchange, the leading application must propagate their tenant JWT token to Document Management Service.

-   Due to the fact that leading application's tenants create repositories using JWT tokens, leading application tenants don't have access to customer repositories.

-   As part of the reuse service approach, the leading application needs to expose our onboarding API.




<a name="loio0f6dd1bbaca342ee9177b9ece3fcaaa3__section_zjf_mgk_jrb"/>

## Application-Managed Multi-Tenancy

-   Leading application handles multi-tenancy.

-   The leading application should send the JWT token of their tenant, not the tenant of their customer.

-   A leading application tenant is onboarded with all repositories.

-   Leading applications are responsible for maintaining a mapping between customers and repositories.

-   These scenarios are appropriate for technical user flow.


**Related Information**  


[Subscribe to Multitenant Applications Using the Cockpit](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/7a3e39622be14413b2a4df7c02ca1170.html?locale=en-US&version=Cloud)

