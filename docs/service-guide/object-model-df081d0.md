<!-- loiodf081d02ad3c4fda9f41fc8bcc4a92c5 -->

# Object Model

CMIS 1.1 defines the following primary base types:

-   Document objects
-   Folder objects
-   Relationship objects
-   Policy objects
-   Item objects

Currently, Document Management Service, Integration Option supports only document and folder objects.

A document object is an item of content. The document can have a content stream, which is the actual file associated with the document. A content stream exists only as part of its containing document object. A content stream has a mime type associated with it. A document object can contain one or more renditions, which are alternative views of the content. Document objects are the only objects that are versionable. Each version of a document has its own object ID. All the versions of a document make up a version series and share a version series ID. You can create, read, update, and delete documents using `OpenCMIS` methods.

A folder object is a container used to organize the document objects. A repository has one root folder. All other folder objects have one parent folder. A folder has a folder path representing its place in the repository's folder hierarchy. A folder object can have renditions. For example, a folder can have a thumbnail as a rendition representing the contents of the folder.

