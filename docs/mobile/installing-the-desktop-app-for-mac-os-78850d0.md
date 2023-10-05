<!-- loio78850d0fd7c74d67a9fd2aad808e49d3 -->

# Installing the Desktop App for Mac OS

The SAP Document Management Service desktop app enables you to comfortably manage your documents and folders across your devices.



<a name="loio78850d0fd7c74d67a9fd2aad808e49d3__prereq_y1w_vk1_zsb"/>

## Prerequisites

-   You've downloaded the desktop client from the SAP Support launchpad. See [Software Downloads](https://launchpad.support.sap.com/#/softwarecenter/template/products/%20_APP=00200682500000001943&_EVENT=DISPHIER&HEADER=Y&FUNCTIONBAR=N&EVENT=TREE&NE=NAVIGATE&ENR=73555000100200016759&V=MAINT&TA=ACTUAL&PAGE=SEARCH/SAP_DOC_MGMT_DESKTOP_APP%201.0). In case you are having trouble accessing the software downloads, check the Knowledge Base article [1613994](https://me.sap.com/notes/1613994)

-   You've configured SAP Identity Authentication for mobile clients. For more information, see [Configuring Identity Authentication In Document Management Service](configuring-identity-authentication-in-document-management-service-cf44481.md).




## Procedure

1.  To start the installation, you've to mount the installation file \(.dmg file\) by double-clicking it.

2.  On the screen that appears, drag and drop the SAP Document Management Service app file \(.app file\) to the *Applications* folder.

3.  Start the desktop app from your *Applications* folder.

4.  On the *Information* screen that appears, read the terms and, if you agree to them, select the *I agree* checkbox. Then choose *Continue*.

5.  On the *Log On* screen that appears, the server URL you entered above is displayed. If you'ven't yet entered a server URL, do so now and choose *Next*.

6.  Depending on the server's settings, the logon methods that are available to you're displayed:

    -   OAuth. For more information, see [Configuring Identity Authentication In Document Management Service](configuring-identity-authentication-in-document-management-service-cf44481.md).

7.  Choose a logon method and enter data as necessary. Then choose *Log On*.

    > ### Note:  
    > If you explicitly choose ![](images/Menu_Log_Off_Icon_ee35401.png)*Log Off* from the app context menu, the *Log On* page appears when you next start the app and you can select a OAuth authentication method. The tray icon changes to gray \(![](images/SDM_Desktop_Client_Application_Status_Disconnected_2951282.png)\). If you choose ![](images/Menu_Exit_Icon_2c00e7e.png)*Exit* to leave the app, the tray icon is closed. The next time you start the app, it logs you on using the authentication mechanism you previously selected \(for example, your client certificate\).

8.  The *Selective Sync* tab of the *Settings* screen that appears gives you the option of defining immediately which folders you want to keep in sync.

9.  You've the option of configuring more settings in the *Settings* window.

    For more information, see [Configuring SAP Document Management Service for Desktop Client](configuring-sap-document-management-service-for-desktop-client-585d79d.md).




<a name="loio78850d0fd7c74d67a9fd2aad808e49d3__result_N100CC_N10011_N10001"/>

## Results

The desktop app starts and tries to authorize your user. The status of the tray icon changes from disconnected \(![](images/SDM_Desktop_Client_Application_Status_Disconnected_2951282.png)\) to synchronizing \(![](images/SDM_Client_Application_Syncronizing_e4b2793.png)\) to log on \(![](images/SDM_Client_Service_Desktop_Icon_b0aa4d2.png)\). You are connected to SAP Document Management Service.

**Related Information**  


[Configuring SAP Document Management Service for Desktop Client](configuring-sap-document-management-service-for-desktop-client-585d79d.md "The SAP Document Management Service desktop app is delivered with a default configuration, which you can adjust using the settings described below.")

[Synchronizing Selected Folders](synchronizing-selected-folders-23bbcdb.md "In the Document Management Service desktop app, you can define which folders are periodically synchronized to your local desktop app.")

[Configuring Identity Authentication In Document Management Service](configuring-identity-authentication-in-document-management-service-cf44481.md "An SAP Business Technology Platform Identity Authentication Service (IAS) is required to authenticate with SAP Document Management Service desktop application for Microsoft Windows and Mac OS.")

