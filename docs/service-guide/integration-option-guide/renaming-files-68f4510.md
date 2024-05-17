<!-- loio68f4510c27eb46a3bdde4c841cc73e1e -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Renaming Files

Learn how to rename files in different scenarios.



## Procedure

1.  For external repositories and version-disabled Document Management Service, Repository Option, choose the <span class="SAP-icons-V5"></span> More Options icon and select *Rename*, make your changes, and save your changes.

2.  For version-enabled Document Management Service, Repository Option, do the steps that follow:

    1.  Select your file.

    2.  Choose *Manage Document* \> *Check Out*.

    3.  If you want, you can download the file and *Rename* it from your local machine.

    4.  Choose *Manage Document* \> *Check In* and select the file to upload a new copy.

    5.  Select version and add your comments.


    > ### Note:  
    > By default, the downloaded file name is the same as the `cmis:ContentStreamFileName`.

    > ### Tip:  
    > You can configure the property [downloadWithContentStreamName](configurations-for-reuse-ui-c91ec16.md#loioc91ec16e80804b91b0b05ea969ea2b87__row_ld5_53k_2xb) to download the file with the `cmis:name`.


