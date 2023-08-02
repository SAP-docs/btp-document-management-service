<!-- loiob978a4de207e4b00a6a1434ec838e86c -->

# Default Encryption via SAP Credential Store

The Document Management Service, Application Option and Document Management Service, Integration Option supports encryption using SAP Credential Store Keyrings.



Encryption in SAP Document Management Service typically refers to a security feature. Encryption allows you to have greater control over the encryption keys used to protect your sensitive data stored within the SAP Document Management Service.



<a name="loiob978a4de207e4b00a6a1434ec838e86c__section_svt_mhq_3xb"/>

## Enable Encryption for Document Management Service, Integration Option 

You can follow the generic steps to add a repository using the Onboarding API in Document Management Service, Integration Option. For more information, see [Onboarding Internal Repository](../integration-option-guide/onboarding-repository-b377990.md#loiob37799034e81433c8312864b0b5a2fab__section_okh_4rz_hrb).

In addition, it necessary to set the parameter `isEncryptionEnabled` to `True` while onboarding internal repository.



### Request Example

```

POST https://<"endpoints" : "ecmservice" : "url">/rest/v2/repositories
```

**Request Body**

> ### Sample Code:  
> ```
> 
> 	{
> 	  "repository": {
> 	    "displayName": "Name of the repository",
> 	    "description": "Description for the repository",
> 	    "repositoryType": "internal",
> 	    "isVersionEnabled": "true",
> 	    "isVirusScanEnabled": "true",
> 	    "skipVirusScanForLargeFile": "false",
> 	    "isThumbnailEnabled": "false",
> 	    "hashAlgorithms": "SHA-256",
> 	    "isEncryptionEnabled": "true"
> 	  }
> 	}
> 
> ```

> ### Remember:  
> -   It's important to note that you don't have any control over the keys if you don't have DCKMS tenant setup, since the key encryption key \(KEK\) is stored in SAP Credential Store.
> 
> -   Enabling encryption is a one-time operation and you can't toggle between `true` or `false` for the parameter `isEncryptionEnabled`.



<a name="loiob978a4de207e4b00a6a1434ec838e86c__section_lwd_rw2_jxb"/>

## Enable Encryption for Document Management Service, Application Option

Document Management Service, Application Option supports encryption via SAP Credential Store. You can enable this feature while creating an internal repository. It's a one-time setting and you can't change it back once the repository has been successfully onboarded. Encryption helps you encrypt all your data stored in the repository securely.

For more information, see [Onboarding Internal Repository](../web-app-guide/onboarding-internal-repository-59e3cb7.md#loio59e3cb769e4f4487a2417d59d65f8276__row_uk4_sbf_jxb).

