<!-- loiofa645de4e5274004ae580408ed260f0c -->

# Consent and Personal Data Record





### User Consent

Data privacy acts require a user consent before storing or processing user's personal data. Document Management Service doesn’t process any personal data. The service allows users with appropriate roles and authorizations, to upload and download files. Users are responsible for the files \(and content\) they upload to, or download from a repository.

> ### Note:  
> Document Management Service doesn't provide the technical capabilities to support the collection, processing, and storage of personal data.

When user creates a document or folder, for the transaction to complete, document properties like who created or modified the document is stored. Therefore, a user who creates or edits documents in Document Management Service needs to be identified with a unique identifier. The unique identifier can be an email ID or username. This information reaches Document Management Service from a secure identity providing systems which Document Management Service doesn't process in any form.

In this case, an explicit user consent isn’t required because Document Management Service doesn't manage or process the user profiles.



### Log Changes to Personal Data

Data privacy acts require applications and platforms to log any changes made to the personal data of users. Document Management Service doesn’t manage user profiles or process any personal data. Even the email ID used in the document properties is fetched from the identity providing systems. There’s no provision in Document Management Service to modify personal data. Hence, the requirement for logging changes in not applicable.



### Information Retrieval

Data privacy acts require a retrieval function that can be used to inform the data subjects about their personal data that is stored or processed. Document Management Service doesn’t manage user profiles or process any personal data. Hence, the requirement for such a retrieval function isn’t applicable.

Additionally, Document Management Service provides a utility to list all the documents and folders that are created or modified by a given user. This utility can be accessed by the Data Protection and Privacy \(DPP\) Admin of Document Management Service, Integration Option and Document Management Service, Application Option.

For Document Management Service, Application Option, a DPP Admin can access the utility in the admin UI.

For Document Management Service, Integration Option, a DPP Admin can access the utility using APIs.



### Erase Personal Data

Data privacy acts require applications and platforms to erase all personal data when the applicable retention periods have expired.

A user who creates or edits documents in Document Management Service needs to be identified with a unique identifier. The unique identifier can be an email ID or username. When the document gets deleted, the associated document properties including the unique identifier get deleted as well.



### Log Read Access to Sensitive Data

Data privacy acts require applications and platforms to log all successful and unsuccessful attempts to read sensitive data using read access logging tools. Document Management Service doesn’t store sensitive data.

Document Management Service doesn't know the content of the documents that users store. In turn, Document Management Service can’t classify the document type as sensitive or not. Hence, Document Management Service doesn't log any attempt to read the documents. Users must know the content of the document before they upload.

SAP’s responsibility as a data processor is limited to the usage of personal data within the SAP products that are subject to the contract. As soon as personal data is in any form extracted or transmitted or transferred manually or via technical interfaces to third-party cloud services, you're responsible to ensure data protection compliance of the third-party.

