<!-- loio1fceb31da2d845d79aa9bf4c98065346 -->

# Configuring Backup

Backup and recovery of data stored in the Document Management Service are performed by SAP. Because Document Management Service doesn't keep a track of data on its own. It makes use of storage systems such as SAP HANA, PostgreSQL on SAP BTP, Hyperscaler Option, and Object Store on SAP BTP.



<a name="loio1fceb31da2d845d79aa9bf4c98065346__section_x2d_4cv_5qb"/>

## Services with Automated Data Backups

Data stored in the following services is automatically backed up by SAP:

-   **SAP HANA Cloud:** SAP HANA Cloud instances are continually backed up to safeguard your database and ensure that it can be recovered. For more information, see [Backup and Recovery](https://help.sap.com/viewer/9ae9104a46f74a6583ce5182e7fb20cb/hanacloud/en-US/89d71f01daca4ecaaa069d6a060167f5.html).

-   **PostgreSQL on SAP BTP, Hyperscaler Option:** SAP keeps backups of your PostgreSQL database instances for a retention period of 14 days. You can restore a database instance to any point in time within the backup retention period by creating a new database instance. For more information, see [Restore Database Instance to a Specified Time](https://help.sap.com/viewer/b3fe3621fa4a4ed28d7bbe3d6d88f036/Cloud/en-US/724c9112ed5a48c59c8e88f17290550d.html).

-   **Object Store on SAP BTP:** Object Store service enables you to use various supported hyperscaler's object store offerings. It enables only the features the underlying hyperscalers already support. For more information, see [Backup and Restore Options](https://help.sap.com/viewer/2ee77ef7ea4648f9ab2c54ee3aef0a29/Cloud/en-US/8c20208a0891482b90bc6192633239b8.html).


