<!-- loio9774430df23140c59c08d773647d9ed0 -->

# Configure Service Account Access

Create and manage service accounts using the Google API console.



<a name="loio9774430df23140c59c08d773647d9ed0__prereq_ycl_v2s_h5b"/>

## Prerequisites

-   You've created a service account in the *Google Cloud* console. For more information about the detailed steps, see [Create a service account](https://developers.google.com/workspace/guides/create-credentials?hl=en#create_a_service_account).

-   You've created a public or private key pair for a service account in the *Google Cloud* console. For more information about the detailed steps, see [Create credentials for a service account](https://developers.google.com/workspace/guides/create-credentials?hl=en#create_credentials_for_a_service_account).




## Context

Service accounts are required to control certain permissions in your Google Workspace account and manage user access, so you need to generate a service account key in the Google API Console.



## Procedure

1.  Navigate to the [Google API Console](https://console.cloud.google.com/cloud-resource-manager?pli=1).

2.  Select your project.

3.  In the left navigation menu, expand *IAM & Admin* \> *Service Accounts*.

4.  At the top of the page, select *Create Service Account*.

5.  Enter a *Service account name* to be displayed in the Google Cloud console.

    > ### Remember:  
    > The service account name generates the *Service account ID* for the account in the console. You can edit the ID in the console itself, but you can't change it later.

6.  **Optional:** Enter a meaningful description of your service account.

7.  Choose *DONE* to finish creating the service account.

    A new service account appears on the project's *Service Accounts* page.

8.  Select the email address of the service account for which you want to create a service account key.

9.  Navigate to the *KEYS* tab at the top.

10. Choose *ADD KEY* \> *Create new key* \> *JSON* \> *CREATE*.

    A JSON key file for your service account is downloaded to your computer. Keep it in a secure location that only you've access to. You won't be able to download the key file again.


**Related Information**  


[Enable the Google Drive API in Your Project](enable-the-google-drive-api-in-your-project-f3a998b.md "For your application to integrate with Google Drive, you need to enable the Google Drive API in your Google Cloud Platform project and provide configuration details.")

[Enable Domain Wide Delegation for the Service Account](enable-domain-wide-delegation-for-the-service-account-c93fea8.md "Manage and authorize your service accounts using domain-wide delegation in the Google Workspace administrator console.")

[Enable Domain Wide Delegation for the Service Account](enable-domain-wide-delegation-for-the-service-account-c93fea8.md "Manage and authorize your service accounts using domain-wide delegation in the Google Workspace administrator console.")

