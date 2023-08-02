<!-- loio8736dd79b4cb4e4092dc2d212553a3cd -->

# Metadata in the Document Management Service

The document store on Document Management Service supports the `cmis:document` and `cmis:folder` types. It also has a built-in subtype for versioned documents. The types can be investigated using the Apache CMIS workbench.

In addition to the standard CMIS properties, the document service of Document Management Service supports additional SAP properties. The most important ones are:

-   `sap:owner` \(the owner of a document\)

    `sap:owner` is used for ACLs \(access control\).

-   `sap:tags`

    `sap:tags` is a multivalued attribute used for tagging the content.


**Related Information**  


[http://chemistry.apache.org/java/download.html](http://chemistry.apache.org/java/download.html)

[http://docs.oasis-open.org/cmis/CMIS/v1.1](http://docs.oasis-open.org/cmis/CMIS/v1.1)

