<!-- loio1c946cc116cc4508942a5d6e455525f9 -->

# Working with Users

You can create required users in your subaccount. When creating a user, you've to provide the identity provider with which the user can be stored.



<a name="loio1c946cc116cc4508942a5d6e455525f9__prereq_fp5_vvp_stb"/>

## Prerequisites

-   You've administration rights in the subaccount. For more information, see [Security Administration: Managing Authentication and Authorization](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/1ff47b2d980e43a6b2ce294352333708.html?locale=en-US&version=Cloud) or [Role Collections and Roles in Global Accounts, Directories, and Subaccounts \[Feature Set B\]](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/0039cf082d3d43eba9200fe15647922a.html?locale=en-US&version=Cloud).

-   You've added the **SDM\_User** role.




## Procedure

1.  Log on to your SAP BTP cockpit and navigate to your subaccount.

2.  Choose *Security* \> *Users*.

3.  Choose *Create*.

4.  Enter the user ID and e-mail address.

5.  Choose the newly created identity provider. The dropdown list displays the identity providers configured in the trust configuration of your subaccount.

6.  Choose *Create*.

    You can now proceed to assign role collections of SAP Document Management service, integration option to the new user. For more information, see [Authorizations](integration-option-guide/authorizations-669d25c.md).


**Related Information**  


[Using SAML Metadata from the Cloud Foundry Account to Copy Location Key](using-saml-metadata-from-the-cloud-foundry-account-to-copy-location-key-74c177a.md "Get the SAML service provider metadata from your Cloud Foundry account.")

