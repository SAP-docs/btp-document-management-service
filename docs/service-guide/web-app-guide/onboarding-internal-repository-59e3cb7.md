<!-- loio59e3cb769e4f4487a2417d59d65f8276 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Onboarding Internal Repository

Connect your Document Management Service, Application Option to Document Management Service, Repository Option for file storage.



<a name="loio59e3cb769e4f4487a2417d59d65f8276__prereq_bzc_h1w_clb"/>

## Prerequisites

-   The global administrator of your SAP BTP account has added the service plan for Document Management Service, Repository Option to your subaccount via entitlements. See [Configure Entitlements for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).

-   You've admin roles assigned to your user profile.




## Procedure

1.  Open the Document Management Service Admin view.

2.  Choose :heavy_plus_sign: *Add Repository*.

3.  In the *Add Repository* dialog box, enter the following parameters as appropriate:


    <table>
    <tr>
    <th valign="top">

    Parameter
    
    </th>
    <th valign="top">

    Required
    
    </th>
    <th valign="top">

    Values
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Repository Type*
    
    </td>
    <td valign="top">
    
    Yes
    
    </td>
    <td valign="top">
    
    *Internal* 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Display Name*
    
    </td>
    <td valign="top">
    
    Yes
    
    </td>
    <td valign="top">
    
    Name of the repository that appears in the application.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Description*
    
    </td>
    <td valign="top">
    
    Optional
    
    </td>
    <td valign="top">
    
    Description of the repository.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Hashing Algorithm*
    
    </td>
    <td valign="top">
    
    Optional
    
    </td>
    <td valign="top">
    
    Lists the supported hashing algorithms to generate content hash for your documents. Acceptable values:

    -   `MD5`

    -   `SHA-1`

    -   `SHA-256`

    -   `None` \(default value\) – choose this option if you don't want to generate content hash.



    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    ions of your documents.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Virus Scan*
    
    </td>
    <td valign="top">
    
    Optional
    
    </td>
    <td valign="top">
    
    Enable the option to scan the documents before you upload them. You can upload files of size up to 400 MB.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Disable for large files*
    
    </td>
    <td valign="top">
    
    Optional
    
    </td>
    <td valign="top">
    
    The option is available only if you enable virus scan. Enable the option to disable virus scan for file size greater than 400 MB.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Collaboration*
    
    </td>
    <td valign="top">
    
    Optional
    
    </td>
    <td valign="top">
    
    Enable the option to create collaboration repositories. For more information, see [Collaboration Repositories for Shared Folders](collaboration-repositories-for-shared-folders-4ac17d4.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Classification*
    
    </td>
    <td valign="top">
    
    Optional
    
    </td>
    <td valign="top">
    
    Enables you to upload different documents and classifies them according to their confidentiality level. For more information, see [Document Classification](../integration-option-guide/document-classification-b8894c2.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Enable Thumbnail*
    
    </td>
    <td valign="top">
    
    Optional
    
    </td>
    <td valign="top">
    
    Displays thumbnail images for files \(PDFs, images, and text files\) you've uploaded.

    > ### Note:  
    > -   Only text, image, and pdf files are supported. There's no support for office documents like MS Word, MS Excel, etc.
    > 
    > -   The feature can only be enabled for newly onboarded repositories; it isn't available for older repositories or repositories that were onboarded previously.
    > 
    > -   It's a one-time setting that needs to be enabled. You can't disable it once you've enabled it.
    > 
    > -   Default thumbnails are displayed for files that don't support thumbnails.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Encryption*
    
    </td>
    <td valign="top">
    
    Optional
    
    </td>
    <td valign="top">
    
    Enable encryption to encrypt your data in the repository.

    > ### Note:  
    > The settings can't be changed once you've onboarded the repository. This is a one-time setting.

    For more information, see [Enable Encryption for Document Management Service, Application Option](../security-topics/sap-managed-key-encryption-b978a4d.md#loiob978a4de207e4b00a6a1434ec838e86c__section_lwd_rw2_jxb).
    
    </td>
    </tr>
    </table>
    
4.  Choose *Add* to consume one block of Document Management Service, Repository Option.


