<!-- loiob8894c20c66342dc82ad9278f60fa81e -->

# Document Classification

You can use document classification to control which actions are available to you in the SAP Document Management service, application option, based on the document confidentiality level.

The SAP Document Management Service enables you to access corporate documents in different ways. You might need to access the important documents from outside the corporate network, you want to restrict the possible actions that can be performed on corporate documents based on their document classification. Therefore, SAP Document Management Service supports enforcing a secure container for confidential documents.

Security policies based on document classification determine the allowed actions. Therefore, you can control the available actions, for example, whether a document can be printed, e-mailed, or opened using a specific program. The policies only apply to documents and repositories, not to folders.

> ### Note:  
> The SAP Document Management Service can only guide the users by providing a security-compliant solution. It can't prevent the intentional violation of security policies by users, for example, by taking screenshots.

Currently, document classification supports a fixed set of security classifications for repositories only. You can classify the confidentiality level for one or all repositories by choosing one of the predefined confidentiality levels in the settings of the administration UI:

-   Strictly Confidential
-   Confidential
-   Internal
-   Customer
-   Public

> ### Note:  
> -   It's a one-time setting that needs to be enabled. You can't disable it once you've enabled it.
> 
> -   There's no default classification available. To set it, you must choose the classification tab via the actions on the UI.

