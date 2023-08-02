<!-- loioc93fea88f3ab47c0944e7668fdfaf206 -->

# Enable Domain Wide Delegation for the Service Account

Manage and authorize your service accounts using domain-wide delegation in the Google Workspace administrator console.



<a name="loioc93fea88f3ab47c0944e7668fdfaf206__prereq_tlx_fbm_qtb"/>

## Prerequisites

-   You've [Super administrator privileges](https://support.google.com/a/answer/2405986#super_admin) for your Google Workspace account.

-   You've granted domain-wide delegation for your service account. For more information about the detailed steps, refer to [Set up domain-wide delegation for a service account](https://developers.google.com/workspace/guides/create-credentials?hl=en#optional_set_up_domain-wide_delegation_for_a_service_account).




## Procedure

1.  Log in to your *Google Admin* console.

2.  On the Admin console home page, navigate to the *Security* \> *API controls*.

3.  Choose *Manage Domain-Wide Delegation*.

4.  Choose *Add new*.

5.  Enter your service account client ID.

    You can find the client ID for your service account on the Service accounts page.

6.  In OAuth Scopes, add each scope that the application can access. In this field, enter `https://www.googleapis.com/auth/drive`.

7.  Choose *Authorize*.


**Related Information**  


[Enable the Google Drive API in Your Project](enable-the-google-drive-api-in-your-project-f3a998b.md "For your application to integrate with Google Drive, you need to enable the Google Drive API in your Google Cloud Platform project and provide configuration details.")

[Configure Service Account Access](configure-service-account-access-9774430.md "Create and manage service accounts using the Google API console.")

[Creating HTTP Destinations](creating-http-destinations-2b04ac7.md "Create destinations in your SAP BTP subaccount to connect Google Drive with Document Management Service, Integration Option.")

