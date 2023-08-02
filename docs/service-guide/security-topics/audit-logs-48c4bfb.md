<!-- loio48c4bfb13a7e425689e784a73b671891 -->

# Audit Logs

Document Management Service writes entries into the audit log of the consumer account for the following operations:



<a name="loio48c4bfb13a7e425689e784a73b671891__section_bj2_clb_cnb"/>

## Repository Operations

Audit-log message category: `ConfigurationChangeAuditMessage`

-   Onboarding a repository

-   Updating a repository

-   Deleting a repository




<a name="loio48c4bfb13a7e425689e784a73b671891__section_hrn_mwz_dnb"/>

## Document Operations

Audit-log message category: `ConfigurationChangeAuditMessage`

-   Creating a document

-   Reading a document

-   Updating a document

-   Deleting a document




<a name="loio48c4bfb13a7e425689e784a73b671891__section_hjz_gwz_dnb"/>

## Configurations

Configurations includes operations like virus scanning, changes to ACL properties.

Audit-log message category: `ConfigurationChangeAuditMessage`

-   Creating a configuration

-   Updating a configuration

-   Deleting a configuration




<a name="loio48c4bfb13a7e425689e784a73b671891__section_ndp_lxz_dnb"/>

## Invalid Login

Audit-log message category: `SecurityEventAuditMessage`

-   Attempts to access Document Management Service with invalid credentials




For more information, see [Audit Log Viewer for the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/e3baa5f1a0c64c44aac8ab3ea3d1b500.html).

