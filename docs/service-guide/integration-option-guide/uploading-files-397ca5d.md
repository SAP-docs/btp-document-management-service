<!-- loio397ca5d9ce6d444baec39181fc43cbcd -->

# Uploading Files

Learn to upload your files to Document Management Service for different scenarios.



## Procedure

1.  To upload files, you must follow one of the steps:

    -   Navigate to the correct folder, select the files, and drag and drop them into the browser window.

    -   Navigate to the correct folder, choose *Create* \> *Document* \> *Upload File*, and select the files to upload.


    > ### Remember:  
    > -   When uploading a large file, *Use multipart* upload. It allows you to upload files larger than 4 GB. If you choose multipart upload, virus scanning is disabled.
    > 
    > -   When we upload files via multipart to versioned repositories, two versions of the document are generated. The first version is a blank document, while the second has actual content.
    > 
    > -   If you're using Document Management Service, Repository Option:
    >     -   With virus scanning disabled – supports upload of file size up to 4 GB.
    > 
    >     -   With virus scanning enabled – supports upload of file size up to 400 MB.

2.  For SAP DMS repositories, you can upload files with a specific document type. Navigate to the correct folder, choose *Create* \> *Document* \> *From Template*, and select the template.

3.  If the folder already contains files with the same name, you must follow one of the steps based on the type of your repository:

    -   For a versioning-disabled repository – you can either *Overwrite files* or *Upload as new files*.

    -   For a versioning-enabled repository – you can either *Check In the Uploaded Changes* or *Upload a New Copy*.



