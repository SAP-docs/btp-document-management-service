<!-- loio717ac5d8de314007a2e23de9ea526aec -->

# Restrictions and Limits

The restrictions and limitations of Document Management Service, Repository Option are listed here.

Understanding these limitations helps you to achieve an optimal use of the service.

> ### Note:  
> The limitations mentioned here are subjected to change.



<a name="loio717ac5d8de314007a2e23de9ea526aec__section_g4g_fxb_xlb"/>

## Limitations on CMIS Features

The following features, which are defined in the OASIS CMIS standard, aren’t supported:

-   Multifiling

-   Policies

-   Relationships

-   Query: Supports only metadata searches. Joins and type aliases aren't supported.




<a name="loio717ac5d8de314007a2e23de9ea526aec__section_n3g_3xb_xlb"/>

## Limitations on Document Properties

-   While making a CMIS query to search documents, for searchable properties – you can send a maximum of 100 values in the query. The maximum character limit for the query is 5,000.

-   While making a CMIS query to search documents, for nonsearchable properties – you can send a maximum of 1,000 values in the query. The maximum character limit for the query is 50,000.

-   Maximum character limit for one property is 4,500.

-   A maximum of 500 major or minor or both versions of a document are supported.

-   At the repository level, allowable queryable properties are restricted to 50 excluding the basic queryable properties provided by CMIS.




<a name="loio717ac5d8de314007a2e23de9ea526aec__section_ewh_3xb_xlb"/>

## Restrictions Due to Virus Scanning

For virus-scanning enabled repositories:

-   You can upload a file of size up to 400 MB.

-   Supports scanning the files only during upload and not during download.

-   If you're using the append content stream or multipart feature to upload a file, virus scanning is disabled.

-   The following restriction must be valid with append content stream:

    -   The maximum file size that can be supported is 50 GB.

    -   Chunk sizes must be 5–100 MB, except for the last chunk.

    -   The last chunk file can be less than 5 MB.

    -   Virus scanning is disabled for documents uploaded using the append content APIs.





<a name="loio717ac5d8de314007a2e23de9ea526aec__section_lbj_3xb_xlb"/>

## Maximum Limit Criteria

-   Unique name of the repository is limited to 100 characters.

-   Maximum duration of 60 seconds for a single CMISQL query.

-   In the Reuse UI, only 50,000 objects are shown for a given folder.

-   A folder hierarchy can have a maximum depth of 150 levels.

-   For query methods like *<IN\_TREE\>*, the search is breadthwise, so only 1000 folders are searched in a breadthwise order.




<a name="loio717ac5d8de314007a2e23de9ea526aec__section_w12_4jv_nsb"/>

## Limitation of the Recycle Bin

When you delete versions of a document directly by selecting the delete option and you can't restore them from the recycle bin because deleting them directly from the version section is treated as a permanent delete.



<a name="loio717ac5d8de314007a2e23de9ea526aec__section_lqb_zqy_jvb"/>

## Append Content Stream Restrictions

The Document Management Service, Repository Option on the Google Cloud Platform supports appending content streams. It's recommended that the first chunk uploaded or the original file shouldn't exceed 100 MB.

