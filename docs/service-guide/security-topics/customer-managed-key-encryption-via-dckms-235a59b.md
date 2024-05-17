<!-- loio235a59b9549b490bbc1908e985abf954 -->

# Customer-Managed Key Encryption via DCKMS

Document Management Service uses SAP Credential store that integrates with SAP Data Custodian Key Management Service \(DCKMS\) to provide you with key management solutions.



<a name="loio235a59b9549b490bbc1908e985abf954__section_dmh_c2s_sxb"/>

## Prerequisites

-   You've onboarded the SAP Data Custodian Key Management Service \(DCKMS\) tenant. See [Key Management Service Administration Guide](https://help.sap.com/docs/sap-data-custodian/key-management-service/administration?locale=en-US).

-   A tenant's subaccount ID should be available in the access token for multitenant applications that consume Document Management Service. See [Multi-Tenancy with Document Management Service](../integration-option-guide/multi-tenancy-with-document-management-service-0f6dd1b.md).



<a name="loio235a59b9549b490bbc1908e985abf954__section_krw_5rw_pxb"/>

## Context

> ### Remember:  
> If you want to encrypt your data using the DCKMS tenant, you must purchase this service separately. It is not included in the Document Management Service subscription model. This ensures that you have full control over the encryption measures you choose for your data.

Customer-Controlled Encryption Key \(CCEK\) scenarios allow you to create and manage encryption keys within your SAP Data Custodian Key Management Service \(DCKMS\) tenant. Credentials stored in the SAP Credential Store can be encrypted with customer-owned keys in the DCKMS tenant and they need to be associated with the end user's tenant subaccount ID in the SAP BTP cockpit.

In the context of SAP Business Technology Platform, Customer-Managed Keys enable customers to manage the lifecycle of the encryption keys used for data encryption at rest. It means you can create, rotate, and revoke encryption keys according to your security policies and compliance requirements.

The primary benefits of using encryption include:

-   **Enhanced data security:** By managing your own encryption keys, you can ensure that your data is encrypted using strong cryptographic algorithms and keys that meet your organization's security standards.

-   **Compliance with regulations:** Some organizations and industries require strict control over the encryption keys used to protect sensitive data. CMKs allow you to comply with these regulations by giving you full control over key management.

-   **Key rotation:** You can regularly rotate encryption keys to minimize the risk of unauthorized access to your data because of compromised keys.

-   **Key revocation:** If a key is compromised or no longer needed, you can revoke it, rendering the data encrypted with that key inaccessible.




### How Does SAP Credential Store Integration Work with DCKMS?

-   SAP Credential Store picks up the subaccount ID associated with a keyring and maps it to the corresponding global account and DCKMS tenant.

-   If SAP Credential Store finds a DCKMS tenant and a Customer-Managed Key \(default subaccount key\), it uses this key to encrypt its own keys.


> ### Remember:  
> -   The SAP Credential Store uses its own keys for encryption when there's no DCKMS tenant setup.
> 
> -   Access to contents encrypted with this key isn't available if you disable the key maintained in the DCKMS tenant.

For more information, see [Customer-Controlled Encryption Key \(CCEK\) Scenarios](https://help.sap.com/docs/SAP_DATA_CUSTODIAN/538dde61cf134c89bda1c31100a6c0e1/02cbd1eb01f247828adeafb84a8e2f65.html) and [Key Management Service Administration Guide](https://help.sap.com/docs/sap-data-custodian/help-guide/key-management-service-administration-guide?version=2303).



<a name="loio235a59b9549b490bbc1908e985abf954__section_r1q_42s_sxb"/>

## Glossary

The following terms are frequently used when you're using the DCKMS tenant.


<table>
<tr>
<th valign="top">

Term

</th>
<th valign="top">

Definition

</th>
</tr>
<tr>
<td valign="top">

Customer-Controlled Encryption Key \(CCEK\)

</td>
<td valign="top">

CCEK scenarios allow you to create and manage encryption keys within your tenant.

</td>
</tr>
<tr>
<td valign="top">

Data Encryption Key \(DEK\)

</td>
<td valign="top">

An encryption key that is used to encrypt and decrypt data.

</td>
</tr>
<tr>
<td valign="top">

Key Encryption Key

</td>
<td valign="top">

An encryption key that is used to encrypt and decrypt a DEK.

</td>
</tr>
<tr>
<td valign="top">

Keyring

</td>
<td valign="top">

A multiversion cryptographic key used to encrypt or decrypt another cryptographic key.

</td>
</tr>
<tr>
<td valign="top">

Symmetric key

</td>
<td valign="top">

Symmetric key encryption is used to encrypt data at rest – for example, in databases or data storage.

</td>
</tr>
<tr>
<td valign="top">

Asymmetric key

</td>
<td valign="top">

The asymmetric key approach uses a pair of keys – known as a public key and a private key–to encrypt and decrypt the data.

</td>
</tr>
</table>

