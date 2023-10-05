<!-- loio1fceb31da2d845d79aa9bf4c98065346 -->

# Configuring Backup

Backup and recovery of data stored in the Document Management Service are performed by SAP. Because Document Management Service doesn't keep a track of data on its own.

Document Management Service makes use of storage systems as follows:

-   **SAP HANA Cloud**: For storing configurations related to the Document Management Service, Integration Option.

-   **PostgreSQL on SAP BTP, Hyperscaler Option**: For storing object metadata related to the Document Management Service, Repository Option.

-   **Object Store on SAP BTP**: For storing object content related to the Document Management Service, Repository Option.




<a name="loio1fceb31da2d845d79aa9bf4c98065346__section_x2d_4cv_5qb"/>

## Service-Specific Backup and Recovery Strategies

-   **SAP HANA Cloud**: SAP HANA Cloud instances are continually backed up to safeguard your database and ensure that it can be recovered. For more information, see [Backup and Recovery](https://help.sap.com/viewer/9ae9104a46f74a6583ce5182e7fb20cb/hanacloud/en-US/89d71f01daca4ecaaa069d6a060167f5.html).

-   **PostgreSQL on SAP BTP, Hyperscaler Option**: SAP keeps backups of your PostgreSQL database instances for a retention period of 14 days. You can restore a database instance to any point in time within the backup retention period by creating a new database instance. For more information, see [Restore Database Instance to a Specified Time](https://help.sap.com/viewer/b3fe3621fa4a4ed28d7bbe3d6d88f036/Cloud/en-US/724c9112ed5a48c59c8e88f17290550d.html).

-   **Object Store on SAP BTP**: Object Store service enables you to use various supported hyperscaler's object store offerings. It enables only the features the underlying hyperscalers already support. For more information, see [Backup and Restore Options](https://help.sap.com/docs/object-store/object-store-service-on-sap-btp/backup-and-restore?locale=en-US).


