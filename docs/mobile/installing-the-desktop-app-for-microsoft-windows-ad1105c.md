<!-- loioad1105cad0cf436fab0a32b67eaae829 -->

# Installing the Desktop App for Microsoft Windows

The SAP Document Management Service desktop app enables you to comfortably manage your documents and folders across your devices.



## Prerequisites

-   You've downloaded the desktop client from the SAP Support launchpad. See [Software Downloads](https://launchpad.support.sap.com/#/softwarecenter/template/products/%20_APP=00200682500000001943&_EVENT=DISPHIER&HEADER=Y&FUNCTIONBAR=N&EVENT=TREE&NE=NAVIGATE&ENR=73555000100200016759&V=MAINT&TA=ACTUAL&PAGE=SEARCH/SAP_DOC_MGMT_DESKTOP_APP%201.0). In case you are having trouble accessing the software downloads, check the Knowledge Base article [1613994](https://me.sap.com/notes/1613994).

-   You've configured SAP Identity Authentication for mobile clients. For more information, see [Configuring Identity Authentication In Document Management Service](configuring-identity-authentication-in-document-management-service-cf44481.md).




## Procedure

1.  To start the installation wizard, double-click the installation file.

2.  On the entry screen of the installation wizard, choose *Next*.

3.  Select the *SAP Document Management Service* checkbox. Optionally, select the *Creates a desktop icon for SAP Document Management Service*, and choose *Next*.

4.  Select the installation folder for SAP Document Management Service \(we recommend that you keep the default\) and choose *Next*.

5.  Enter the server URL and choose *Next*.

6.  Once the installation is finished, choose *Close*.

7.  Start the desktop app by using the desktop icon \(![](images/SDM_Client_Service_Desktop_Icon_b0aa4d2.png)\).

8.  On the *Information* screen that appears, read the terms and, if you agree to them, select the *I agree* checkbox. Then choose *Continue*.

9.  On the *Log On* screen that appears, the server URL you entered above is displayed. If you haven't yet entered a server URL, do so now and choose *Next*.

10. Depending on the server's settings, the logon methods that are available to you're displayed:

    -   OAuth. For more information, see [Configuring Identity Authentication In Document Management Service](configuring-identity-authentication-in-document-management-service-cf44481.md).

11. Choose a logon method and enter data as necessary. Then choose *Log On*.

    > ### Note:  
    > If you explicitly choose ![](images/Menu_Log_Off_Icon_ee35401.png)*Log Off* from the app context menu, the *Log On* page appears when you next start the app and you can select a OAuth authentication method. The tray icon changes to gray \(![](images/SDM_Desktop_Client_Application_Status_Disconnected_2951282.png)\). If you choose ![](images/Menu_Exit_Icon_2c00e7e.png)*Exit* to leave the app, the tray icon is closed.

12. The *Selective Sync* tab of the *Settings* screen that appears gives you the option of defining immediately which folders you want to keep in sync.

    Alternatively, you can choose which folders to keep in sync later on using the *Settings* entry in the context menu of the tray icon.

13. You've the option of configuring more settings in the *Settings* window.

    For more information, see [Configuring SAP Document Management Service for Desktop Client](configuring-sap-document-management-service-for-desktop-client-585d79d.md).




<a name="loioad1105cad0cf436fab0a32b67eaae829__result_N100CC_N10011_N10001"/>

## Results

The desktop app starts and tries to authorize your user. The tray icon status changes from disconnected \(![](images/SDM_Desktop_Client_Application_Status_Disconnected_2951282.png)\) to synchronizing \(![](images/SDM_Client_Application_Syncronizing_e4b2793.png)\) to log on \(![](images/SDM_Client_Service_Desktop_Icon_b0aa4d2.png)\). You're connected to SAP Document Management Service.

**Related Information**  


[Configuring SAP Document Management Service for Desktop Client](configuring-sap-document-management-service-for-desktop-client-585d79d.md "The SAP Document Management Service desktop app is delivered with a default configuration, which you can adjust using the settings described below.")

[Synchronizing Selected Folders](synchronizing-selected-folders-23bbcdb.md "In the Document Management Service desktop app, you can define which folders are periodically synchronized to your local desktop app.")

[Configuring Identity Authentication In Document Management Service](configuring-identity-authentication-in-document-management-service-cf44481.md "An SAP Business Technology Platform Identity Authentication Service (IAS) is required to authenticate with SAP Document Management Service desktop application for Microsoft Windows and Mac OS.")

