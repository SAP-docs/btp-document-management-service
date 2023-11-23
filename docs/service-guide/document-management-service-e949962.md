<!-- loioe9499627f90549a0ad6a77661b62fa66 -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Document Management Service





**Core Components, 2023**


<table>
<tr>
<th valign="top">

Technical Component

</th>
<th valign="top">

Environment

</th>
<th valign="top">

Title

</th>
<th valign="top">

Description

</th>
<th valign="top">

Action

</th>
<th valign="top">

Lifecycle

</th>
<th valign="top">

Type

</th>
<th valign="top">

Line of Business

</th>
<th valign="top">

Modular Business Process

</th>
<th valign="top">

Product

</th>
<th valign="top">

Latest Revision

</th>
<th valign="top">

Available as of

</th>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Root Certificate Replacement

</td>
<td valign="top">

Following the announcement of the [root certificate replacement](https://help.sap.com/whats-new/cf0cb2cb149647329b5d02aa96303f56?Valid_as_Of=2023-05-04%3A2023-05-04&locale=en-US&version=Cloud) in the SAP Business Technology Platform, if you're consuming SAP Document Management Service, Integration Option via SAP S/4HANA integration \(an outbound scenario where SAP Document Management Service is a repository\) needs to be updated with a new certificate.

For more information, see SAP Note [3327214](https://me.sap.com/notes/3327214) and the [Changing the SAP BTP Cloud Foundry environment Root Certificate Authority](https://blogs.sap.com/2023/10/11/changing-the-sap-btp-cloud-foundry-environment-root-certificate-authority/) blog post.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-11-01

</td>
<td valign="top">

2023-11-01

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Release Update

</td>
<td valign="top">

In this release, we've fixed some bugs and provided security updates. This release doesn't include any new features.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-10-06

</td>
<td valign="top">

2023-10-06

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Contribute to the help documentation content and share your feedback on GitHub.

</td>
<td valign="top">

You now have the opportunity to contribute to this guide by providing feedback through GitHub. On the SAP Help Portal, a new Feedback feature enables you to share your thoughts with the authors in charge and the development team and discuss any documentation-related issues. To use this feature, you must have a GitHub account. For more information, see[What Is Document Management Service?](what-is-document-management-service-27e742e.md) and [SAP BTP Documentation Goes GitHub: Learn About Our New Collaboration Process](https://www.youtube.com/watch?v=WJ0oarMlVW4).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-08-10

</td>
<td valign="top">

2023-08-10

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Updates in the Public Share

</td>
<td valign="top">

If you enable public sharing for folders in your collaboration repositories by default a Guest user with reader permission is added. The guest user can't change or modify documents with only reader permission. They'll only be able to view the shared documents. Administrators can control guest user permissions via write permission, which enables the *Guest* as a *Contributor* to the public share. However, explicitly adding the ACL property `{sap:builtin}anonymous` isn't allowed via the UI. 

See [Create a Shared Folder and Define Its Access](integration-option-guide/create-a-shared-folder-and-define-its-access-1ceb1c8.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-07-13

</td>
<td valign="top">

2023-07-13

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Migrating a Document

</td>
<td valign="top">

A single document can now be copied when migrating between repositories. This simplifies the migration process and reduces the amount of time needed to complete it. It also ensures that the data remains intact during the migration process. This feature is available in both Document Management Service, Integration Option and Document Management Service, Application Option.

See [API](https://api.sap.com/api/MigrationAPI/path/post_copy) and [Migrating Between Repositories](web-app-guide/migrating-between-repositories-0feb51b.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-07-13

</td>
<td valign="top">

2023-07-13

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

ACL Update

</td>
<td valign="top">

Formerly, when you added or removed a principal in Access Control, the following properties were updated. Access Control \(ACL\) has changed the behavior of the properties *Modified Date* and *Modified By*, so they'll no longer refresh when new ACLs are added or removed from collaboration or shared folders. Versioning tracks any changes to metadata or content.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-07-13

</td>
<td valign="top">

2023-07-13

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

UI Improvement

</td>
<td valign="top">

You can onboard the favorite repository only once per service instance of your Document Management Service, Application Option. We've introduced a tooltip to clarify this. If you're already onboarded for the favorite repository, you'll see the disabled radio button. In the tooltip, you're informed that the favorite repository already exists.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-07-13

</td>
<td valign="top">

2023-07-13

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Format of Adding Principals with Role Collections in the Access Control.

</td>
<td valign="top">

Access control now allows multiple principles to be added with a space. With this release, you'ren't required to use white space rather you can add semicolon \(;\) to add the role collections in the group name.

For example, you can use the group name as `~group~Hiring Managers;`

See [Assigning Role Collections in Access Control](integration-option-guide/assigning-role-collections-in-access-control-1d22b1c.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-06-15

</td>
<td valign="top">

2023-06-15

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Encryption

</td>
<td valign="top">

Document Management Service, Integration Option and Document Management Service, Application Option offer support for encryption. You can encrypt your information by enabling encryption using UI and API. Encryption helps protect your data and keeps it secure.

See [Encryption](security-topics/encryption-6ec1122.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-06-15

</td>
<td valign="top">

2023-06-15

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Using Email Address in the Access Control Principals

</td>
<td valign="top">

Email addresses are case-insensitive when you add user email addresses in the *Access Control* as principals.

You can add email addresses without modifying the cases. This means that you don't have to worry about typing the same case as the original email address. For example, if the original email address is john@example.com, you can add it as John@example.com or even jOhN@example.com.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-06-15

</td>
<td valign="top">

2023-06-15

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Thumbnail Support for Older Repositories

</td>
<td valign="top">

You can now enable thumbnails for the documents present in the older repositories in both Document Management Service, Integration Option and Document Management Service, Application Option.

It will generate a thumbnail for the respective documents available in older repositories after a successful sync of repositories metadata. The thumbnail is available in the new repository to make the documents easier to identify. The process will also ensure that the documents are secure and accessible only to authorized users.

-   For Document Management Service, Application Option, after enabling the thumbnail on the repository and synchronizing metadata, the *Generate Thumbnail* button appears for all documents. All you've to do is navigate to the *More Options* and choose the *Generate Thumbnail* option for the particular document.

-   For Document Management Service, Integration Option, enable thumbnails by updating the repository via API [Update Repository](https://api.sap.com/api/AdminAPI/resource/Update_a_Repository) followed by [Sync a Repository](https://api.sap.com/api/AdminAPI/resource/Sync_a_Repository) and then use [Generate Thumbnail](https://api.sap.com/api/GenerateThumbnailApi/resource/Generate_Thumbnail) for the documents.

    See [Generating Thumbnail](key-features/repo-features/generating-thumbnail-c6de2be.md).




</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-06-15

</td>
<td valign="top">

2023-06-15

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Public Share UI Text Update

</td>
<td valign="top">

The default principal *\{sap:builtin\}anonymous* that appears in share settings has been renamed to *Guest*.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-06-15

</td>
<td valign="top">

2023-06-15

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Update

</td>
<td valign="top">

The Feature Scope Description guide has been updated to include encryption security features.

See [Feature Scope Description](https://help.sap.com/doc/4551b91432244b9586798187207100a7/Cloud/en-US/Document_Management_FSD.pdf).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-06-15

</td>
<td valign="top">

2023-06-15

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Update About APIs

</td>
<td valign="top">

The title of the SAP Document Management Service REST APIs has been renamed from *SAP Document Management Service, Integration Option – Content Management Interoperability Services* to *SAP Document Management Service, Integration Option - CMIS*. It provides an overview of the available APIs and how to use them.

See API published on [SAP Business Accelerator Hub](https://api.sap.com/package/SAPDocumentManagementServiceIntegrationOptionCMISAPI/rest).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-06-15

</td>
<td valign="top">

2023-06-15

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Support for Encryption and Security Classification options in Migration

</td>
<td valign="top">

For the target repositories, migration features offer *Encryption* and *Security Classification*.

-   For Document Management Service, Application Option, see [Migrating to SAP Document Management Service](web-app-guide/migrating-to-sap-document-management-service-2f448be.md).

-   For Document Management Service, Integration Option, see [Migration Operations API](https://api.sap.com/api/MigrationAPI/overview).




</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-06-15

</td>
<td valign="top">

2023-06-15

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Other



</td>
<td valign="top">

Document Management Service iOS Mobile App - New Version

</td>
<td valign="top">

The SAP Document Management Service iOS app has been updated to version **23.04.1**. Deep links support has been enhanced for the iOS app with this release. This enhancement allows users to quickly access documents, folders, and other items directly from within the app.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service Mobile Clients

</td>
<td valign="top">

2023-05-22

</td>
<td valign="top">

2023-05-22

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Thumbnail Support

</td>
<td valign="top">

You can now enable thumbnails for older repositories in Document Management Service, Integration Option. The thumbnail option can be enabled for existing repositories. All new documents have thumbnails-generated \(supported mime types \*.txt, image, and pdf\) via `createDocument`. To enable thumbnails for existing documents, refer to the `Generate Thumbnail` API published on [SAP Business Accelerator Hub](https://int.api.hana.ondemand.com/api/GenerateThumbnailApi/resource/Generate_Thumbnail).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service, Integration Option

</td>
<td valign="top">

2023-05-18

</td>
<td valign="top">

2023-05-19

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

UI Improvements

</td>
<td valign="top">

-   The *Share with members* checkbox for Share Folders in the Collaboration repository has been removed. By default, the Share Folder is a member share.

-   The *Share settings* tab is removed from the children of the public shares of the collaboration repository.



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-05-18

</td>
<td valign="top">

2023-05-18

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Using Google Private Key in the Destinations

</td>
<td valign="top">

With this release, replacing the character [/n\] in the private key is no longer necessary. You can directly paste the Google private key into the destination property. It has no impact on existing destinations, and you don't need to take action.

See [Creating HTTP Destinations](creating-http-destinations-2b04ac7.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-04-20

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Renaming Files

</td>
<td valign="top">

Reuse UI now allows you to configure a property for downloading files with `cmis:name`.

When using the Document Management Service, Application Option, the document download is set to `ContentStreamFileName` by default.

See [Configurations for Reuse UI](integration-option-guide/configurations-for-reuse-ui-c91ec16.md) and [Renaming Files](integration-option-guide/renaming-files-68f4510.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-04-20

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Share Settings

</td>
<td valign="top">

Prior to this update, the *Hide uploaded files* option in Document Management Service, Application Option was integrated with the *Write permission* in the public *Share Settings*. Now, the option to hide uploaded files can be enabled independently, and it has been designed to enable users to hide only the necessary files while using the public share.

See [Create a Shared Folder and Define Its Access](integration-option-guide/create-a-shared-folder-and-define-its-access-1ceb1c8.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-03-23

</td>
<td valign="top">

2023-03-23

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Edit Link

</td>
<td valign="top">

If you use a link file in the versioned repository of Document Management Service, Application Option, you're n't required to *Check-In* and *Check-Out* like earlier. It's as simple as clicking the *Edit Link* option to make changes. The change is only applicable to links and other types of documents continue to support the *Check-In* and *Check-Out* functions.

See [Creating External Links](integration-option-guide/creating-external-links-a16dddc.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-03-23

</td>
<td valign="top">

2023-03-23

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Version Update

</td>
<td valign="top">

The SAP Document Management Service desktop application has been upgraded to the version 2.0.6 in both Windows and Mac operating systems.

A bug fix for Outlook integration is included in this version.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-03-02

</td>
<td valign="top">

2023-03-02

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

REST API Update

</td>
<td valign="top">

The `Get Folder Tree` REST API response is now sorted based on `cmis:name`.

Refer to the updated API published on [SAP Business Accelerator Hub](https://api.sap.com/api/GetFolderTreeApi/resource).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-02-23

</td>
<td valign="top">

2023-02-23

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

UI Improvements

</td>
<td valign="top">

A new <span class="SAP-icons"></span> *More Options* section allows you to access actions like Show Properties, Rename, and Preview.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-02-23

</td>
<td valign="top">

2023-02-23

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Document Classification Support

</td>
<td valign="top">

We've now added document classification support to older repositories. If you've older repositories, you can check and enable document classification and assign a classification to the documents.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-02-23

</td>
<td valign="top">

2023-02-23

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Permission Changes in the Access Control Lists

</td>
<td valign="top">

The permissions have been renamed from technical to more user-friendly names in an effort to simplify the permission assignment process. No changes have been made to the functionalities.

**Access Control Lists**


<table>
<tr>
<th valign="top">

Old Name

</th>
<th valign="top">

New Name

</th>
</tr>
<tr>
<td valign="top">

`cmis:read`

</td>
<td valign="top">

*Reader*

</td>
</tr>
<tr>
<td valign="top">

`sap:file`

</td>
<td valign="top">

*Creator*

</td>
</tr>
<tr>
<td valign="top">

`cmis:write`

</td>
<td valign="top">

*Editor*

</td>
</tr>
<tr>
<td valign="top">

`sap:delete`

</td>
<td valign="top">

*Contributor*

</td>
</tr>
<tr>
<td valign="top">

`cmis:all`

</td>
<td valign="top">

*Administrator*

</td>
</tr>
</table>

See [Access Control Lists](integration-option-guide/access-control-lists-01fb63b.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-02-23

</td>
<td valign="top">

2023-02-23

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Document Management Service iOS Mobile Client - New Version

</td>
<td valign="top">

The SAP Document Management Service iOS app has been updated to version 16.0.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-02-23

</td>
<td valign="top">

2023-02-23

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Support for Subscription -Based Commercial Model

</td>
<td valign="top">

The Document Management Service, Application Option no longer supports the subscription-based commercial model. You can only purchase it through a consumption-based commercial model.

See [Pricing Information for Document Management Service, Application Option](https://discovery-center.cloud.sap/serviceCatalog/document-management-service-application-option?service_plan=standard&region=all&commercialModel=cpea&tab=service_plan).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-01-25

</td>
<td valign="top">

2023-01-25

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Android Version Upgrade

</td>
<td valign="top">

The SAP Document Management Service Android app has been updated to version 8.0.

See [Installing the Android App](https://help.sap.com/viewer/774c31c426df4fee9cbdcee9bbd876f8/Dev/en-US/16623553fdb8487b8e09f265f1fce347.html "Before you can use the Document Management Service mobile app on your Android device, you've to set it up.") :arrow_upper_right:.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-01-25

</td>
<td valign="top">

2023-01-25

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Content Server Download

</td>
<td valign="top">

If you want to download files directly from the content server while updating your own repositories, use the *Content Server Download* option in the Document Management Service, Application Option.

See [Update Your Own Repository](web-app-guide/update-your-own-repository-dc0a791.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2023-01-25

</td>
<td valign="top">

2023-01-25

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Document Classification

</td>
<td valign="top">

Applying security policies allows you to classify documents according to their confidentiality level. The feature is available in both the Document Management Service, Application Option and the Document Management Service, Integration Option.

See [Document Classification](integration-option-guide/document-classification-b8894c2.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2022-12-02

</td>
<td valign="top">

2022-12-02

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Thumbnail

</td>
<td valign="top">

The Document Management Service, Application Option and Document Management Service, Integration Option now support the usage of thumbnails that shows the thumbnail images for files \(PDFs, texts, and images\).

See [Onboarding Internal Repository](web-app-guide/onboarding-internal-repository-59e3cb7.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2022-12-02

</td>
<td valign="top">

2022-12-02

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Availability of Document Management Service, Repository Option 

</td>
<td valign="top">

The Document Management Service, Repository Option is now available on Google Cloud Platform \(region cf US-30 and EU-30\).

See [Service Plans](service-plans-944c578.md) and [Restrictions and Limits](restrictions-and-limits-717ac5d.md) .

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

Document Management Service

</td>
<td valign="top">

2022-11-04

</td>
<td valign="top">

2022-11-04

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP Document Management Service Outlook Add-In

</td>
<td valign="top">

A new Microsoft Outlook add-in feature has been introduced for the SAP Document Management Service desktop client, which lets you automatically create, share, and include links in emails. A secure email is a great way to store and share files for your meetings.

See [Sending Mail Attachments Using the Microsoft Outlook Add-In](https://help.sap.com/viewer/774c31c426df4fee9cbdcee9bbd876f8/Dev/en-US/a5f77e4b10bb4700907576c4afa05caa.html "Document Management Service offers a Microsoft Outlook add-in that can automatically create a share, include a link to the share in your mail or meeting request, and store the files you want to attach to your mail or meeting request in this share. In this way, you can attach files that exceed your allowed mail attachment size limit.") :arrow_upper_right:.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2022-10-14

</td>
<td valign="top">

2022-10-14

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Release Update

</td>
<td valign="top">

This release includes some bug fixes, performance improvements, and security updates. This version doesn't include any new features.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2022-09-09

</td>
<td valign="top">

2022-09-09

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

REST API for Offboarding Repository

</td>
<td valign="top">

REST-based APIs now let you off-board your repository as well as check the status of offboarding and download repository data.

Refer to a new API published on [SAP Business Accelerator Hub](https://api.sap.com/api/AdminAPI/resource).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2022-08-11

</td>
<td valign="top">

2022-08-11

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

REST API for Favorites Repository

</td>
<td valign="top">

REST-based APIs now let you add a repository category called *Favorites*. When onboarding a repository, you can now include Favorites as a separate category. Favorite repositories allow you to quickly access your files and folders.

Check out the Onboard Repository for API references [SAP Business Accelerator Hub](https://api.sap.com/api/AdminAPI/resource).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2022-08-11

</td>
<td valign="top">

2022-08-11

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Favorites Repository Category

</td>
<td valign="top">

The Document Management Service, Application Option as well as the Document Management Service, Integration Option have introduced a new repository category called Favorites.

See [Onboarding Favorites Repository](web-app-guide/onboarding-favorites-repository-015d8a1.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2022-08-11

</td>
<td valign="top">

2022-08-11

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Theme Support for the SAP Document Management Service Mobile Applications

</td>
<td valign="top">

The SAP Document Management Service mobile applications now support dark themes for Android and iOS devices. When you enable a dark theme on your system, the application is automatically supported.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-08-11

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Security Settings in SAP Document Management Service Mobile Applications

</td>
<td valign="top">

The SAP Document Management Service mobile application supports the use of an app passcode on both Android and iOS devices. If you've an iPhone, you can unlock the Document Management service app with a Face ID instead of a passcode, because if you've an Android phone, you can unlock it with a fingerprint.

See [Defining the App Settings (iOS)](https://help.sap.com/viewer/774c31c426df4fee9cbdcee9bbd876f8/Dev/en-US/8ea949d82ae3441ea033ad1e4bbbae94.html "You can define global settings in your mobile app. The options available to you depend on company policy and the settings that your administrator has preselected.") :arrow_upper_right: and[Defining the App Settings (Android)](https://help.sap.com/viewer/774c31c426df4fee9cbdcee9bbd876f8/Dev/en-US/5468c2412201434a860b6e4436530db1.html "You can define global settings in your mobile app. The options available to you depend on company policy and the settings that your administrator has preselected.") :arrow_upper_right: .

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-08-11

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Integrating Google Workspace with Document Management Service, Integration Option 

</td>
<td valign="top">

You can now set up a new integration scenario using Google Workspace for SAP Document Management service, integration option. You can leverage Google Workspace as CMIS-compliant repository and manage your documents and folders. It's possible to manage and store your documents on both shared and personal drives.

See [Integrating SAP S/4HANA with Google Workspace Using SAP Document Management Service](integrating-sap-s-4hana-with-google-workspace-using-sap-document-management-service-594bf95.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-07-14

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Copy and Move Documents

</td>
<td valign="top">

Documents that are searchable can now be moved and copied.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-07-14

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Theme Support for the Document Management Service, Application Option 

</td>
<td valign="top">

You can change the appearance of your Document Management Service, Application Option UI using themes.

See [Accessibility Features in Document Management Service](security-topics/accessibility-features-in-document-management-service-c2007f5.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-07-14

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

UI Improvements

</td>
<td valign="top">

The *Attachments* have been renamed to *Items*. You can see the number of items for all files and folders, and this helps you to get an overview of the documents attached to a particular folder at a glance.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-07-14

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Optional parameter introduced in the third-party migration API

</td>
<td valign="top">

You can use `externalId` as an optional parameter when you're using third-party migration APIs.

See [Migrating Third-Party CMIS Repositories](https://api.sap.com/api/MigrationAPI/resource).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-06-16

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

UI Improvements

</td>
<td valign="top">

It's now possible for you to see the number of attachments for all files and folders, and this helps you to get an overview of the documents attached to a particular folder at a glance.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-06-16

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Delete Migrations

</td>
<td valign="top">

The Delete functionality allows you to remove migrations that are no longer needed or that are unused.

See [Deleting Migrations](web-app-guide/deleting-migrations-d15e69f.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-06-16

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Migration API for Copy Scenario

</td>
<td valign="top">

Using the REST API, you can now copy folder from one repository to another.

See [Copying Folder in SAP Document Management Service Repository to Another](https://api.sap.com/api/MigrationAPI/resource).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-06-16

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Document Management Service, Application Option on Cloud Platform Enterprise Agreement

</td>
<td valign="top">

Document Management Service, Application Option has been added to the Cloud Platform Enterprise Agreement. You can license it according to a consumption-based commercialization model.

See [Concepts](concepts/concepts-0adeaf1.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-05-19

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Support for QR code scanning in SAP Document Management Service mobile applications

</td>
<td valign="top">

Using a QR code, you can now register server URL in the SAP Document Management Service mobile application for Android and iOS.

See [Installing the Android App](https://help.sap.com/viewer/774c31c426df4fee9cbdcee9bbd876f8/Dev/en-US/16623553fdb8487b8e09f265f1fce347.html "Before you can use the Document Management Service mobile app on your Android device, you've to set it up.") :arrow_upper_right: and [Installing the iPad or the iPhone App](https://help.sap.com/viewer/774c31c426df4fee9cbdcee9bbd876f8/Dev/en-US/ffe75ca24d7843138ae3d8bd8fd4e07a.html "Before you can use the Document Management Service mobile app on your iOS device, you've to set it up.") :arrow_upper_right:.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-05-19

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Pagination Support

</td>
<td valign="top">

Page number can be automatically determined based on the number of documents in the view mode by using pagination feature. The feature is available in both the Document Management Service, Application Option and Document Management Service, Integration Option.

See [Configurations for Reuse UI](integration-option-guide/configurations-for-reuse-ui-c91ec16.md) and [Using Pagination](integration-option-guide/using-pagination-b40f283.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-04-21

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP Document Management Service desktop client support for Mac operating system

</td>
<td valign="top">

The SAP Document Management Service desktop application is now available on the Mac operating system, allowing you to manage documents and folders from your desktop.

See [Installing the Desktop App for Mac OS](https://help.sap.com/viewer/774c31c426df4fee9cbdcee9bbd876f8/Dev/en-US/78850d0fd7c74d67a9fd2aad808e49d3.html "The SAP Document Management Service desktop app enables you to comfortably manage your documents and folders across your devices.") :arrow_upper_right:.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-03-30

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Deep links support for both SAP Document Management Service desktop and mobile clients

</td>
<td valign="top">

You can create links that perform actions within the SAP Document Management Service app and can be used for app-to-app integration. You can also use the link as a direct link in emails.

See [URLs for App-to-App Integration of Document Management Service](https://help.sap.com/viewer/774c31c426df4fee9cbdcee9bbd876f8/Dev/en-US/3fbbe2480b3c48f5b306af548a05ad8f.html "You can build URLs that perform actions in the SAP Document Management Service app and that can be used for app-to-app integration or as links in e-mails.") :arrow_upper_right:.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-03-24

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP Document Management Service Android application supports the import of files

</td>
<td valign="top">

You can now import files using SAP Document Management Service Android application.

See [Adding and Deleting Files and Folders (Android)](https://help.sap.com/viewer/774c31c426df4fee9cbdcee9bbd876f8/Dev/en-US/d7c9f53523b4485a9d80a3edce5c2422.html "In the SAP Document Management Service mobile app you can add and delete files and folders.") :arrow_upper_right:.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-03-24

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Third-party CMIS-compliant repositories are supported for SAP Document Management Service clients \(Desktop and Mobile\)

</td>
<td valign="top">

With SAP Document Management Service clients, third-party CMIS-compliant repositories are now supported.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-03-24

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Language Support

</td>
<td valign="top">

The UI texts of support Document Management Service, Application Option Italian language.

See [Supported Languages](concepts/supported-languages-fc3970e.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-03-24

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Tenant Migration API

</td>
<td valign="top">

Using the REST API, selective tenant migration is now supported. Optional 'tenants' field has been added.

See [Migrating Document Service](https://api.sap.com/api/MigrationAPI/resource).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-02-24

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Cross Repository Data Migration API

</td>
<td valign="top">

Through the REST APIs, cross-repository migration is now supported. You can copy data and move it around from one repository to another using the APIs.

See [Copying Folder in SAP Document Management Service Repository to Another](https://api.sap.com/api/MigrationAPI/resource).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-02-24

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Recycle Bin in Document Management Service, Application Option 

</td>
<td valign="top">

Certain limitations apply when it comes to restoring different versions of deleted documents from the recycle bin.

See [Restrictions and Limits](restrictions-and-limits-717ac5d.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-02-24

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Mutual Transport Layer Security \(mTLS\)

</td>
<td valign="top">

You can exchange tokens with the service using mTLS instead of providing the client ID and clientsecret. This method provides better security since clientsecret isn't transmitted with token requests.

See [Enable mTLS Authentication for Document Management Service](security-topics/enable-mtls-authentication-for-document-management-service-5f70318.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-01-31

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Retention Feature in Document Management Service, Application Option 

</td>
<td valign="top">

You can now use Retention feature in the Document Management Service, Application Option to prevent documents from being deleted or modified.

See [Retention](integration-option-guide/retention-f271828.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-01-05

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

UI Improvements

</td>
<td valign="top">

As a paginated response, you can now view a complete list of documents and folders found on a particular item in basic search, advanced search, copy, and move scenarios. Search entries are shown in full and aren't truncated.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-01-05

</td>
</tr>
<tr>
<td valign="top">

Document Management Service

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Recycle Bin

</td>
<td valign="top">

The Recycle Bin now allows you to permanently delete documents and folders.

See [Deleting and Restoring Files and Folders](integration-option-guide/deleting-and-restoring-files-and-folders-af6b72b.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">



</td>
<td valign="top">

2022-01-05

</td>
</tr>
</table>

