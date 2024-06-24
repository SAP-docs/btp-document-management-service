<!-- loioc1c356dda70c491cbd6e7df1f5f368c2 -->

# Installing the iOS App

Before you can use the SAP Document Management mobile app on your iOS device, you have to set it up.



## Context

-   Your iOS device has version 12.0 or higher installed.

-   You already have the QR code for the server URL. For more information, see [Accessing a QR Code for Mobile Applications](accessing-a-qr-code-for-mobile-applications-985ec46.md).

-   You have been assigned the role of `SDM_User` in the SAP BTP subaccount.




## Procedure

1.  Download and install the SAP Document Management app from the Apple App Store. See [SAP Document Management app on Apple App Store](https://apps.apple.com/us/app/document-management-service/id1593443458).

2.  Start the app.

3.  If you're installing the app for the first time, you're asked to review and accept an End User License Agreement and Privacy Statement. Click *Agree*.

4.  Configure your account using a QR code.

    1.  On the iOS device, choose *Scan*.

    2.  With the camera of the iOS device, scan the QR code.

    3.  In the confirmation message, choose *Continue*.

    4.  Authenticate the user by entering their credentials.

        If you're asked to set a passcode to protect the data stored in the app, enter a passcode containing at least 8 characters. This depends on the passcode policy that is set in your SAP Mobile Services instance.

        > ### Caution:  
        > If you forget your passcode, you have to reinstall the app. This means that you have to enter your settings again and all synced documents are lost.


    You're connected to SAP Document Management mobile application.

    You will see a list of repositories. After the mobile application has synced with the instance containing the repositories, you can see the files and the folders in the repositories. The time it takes to sync can vary based on the amount of data.


