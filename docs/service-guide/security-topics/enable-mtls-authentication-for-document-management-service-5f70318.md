<!-- loio5f7031876e474007816c8d3060c51cd0 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Enable mTLS Authentication for Document Management Service

To enable mutual transport layer security \(mTLS\) in Document Management Service, you first need to enable mTLS authentication for the SAP Authorization and Trust Management service. Then make sure that the binding includes the X.509 credentials.



<a name="loio5f7031876e474007816c8d3060c51cd0__prereq_lqw_l4r_hsb"/>

## Prerequisites

You've created an instance of Document Management Service, Integration Option. See [Creating Service Instances in Cloud Foundry](https://help.sap.com/viewer/09cc82baadc542a688176dce601398de/Cloud/en-US/6d6846def3c443aa9f83d127353147ce.html).



## Context

Mutual Transport Layer Security \(mTLS\) is considered more secure than the combination of client ID and clientsecret. In this configuration, the private key isn't shared between calling application and the service instance of SAP Authorization and Trust Management service \(XSUAA\).

In this configuration, your application is able to retrieve or exchange access tokens with an instance of the SAP Authorization and Trust Management service through mTLS. Using the access token, your application can communicate with other services, applications, and devices via the standard OAuth protocol.

You can generate a X509 certificate using the following methods based on your use case:

-   Binding Service Instances to Document Management Service, Integration Option with X509 certificate.

-   Creating service key for cloud foundry application Document Management Service, Integration Option with X509 certificate.


<a name="task_nnk_ymr_hsb"/>

<!-- task\_nnk\_ymr\_hsb -->

## Binding Service Instances to Document Management Service, Integration Option with X509 Certificate

You can bind a service instance with your application using the binding parameters presented in the steps for generating an X509 certificate.



<a name="task_nnk_ymr_hsb__steps_grb_zmr_hsb"/>

## Procedure

1.  In the left navigation area, choose *Services* \> *Instances and Subscriptions*.

2.  On the *Instances and Subscriptions* page, navigate to the *Instances* section and select the instance to which you wish to bind the application.

3.  In the service instance details section that opens to the right, select the Actions menu \(<span class="SAP-icons"></span>\) and then select *Create Binding*.

4.  In the *New Binding* wizard, choose the application to bind and specify the following parameters in JSON format:

    ```json
    
    {
        "xsuaa": {
            "credential-type": "x509",
            "x509": {
                "key-length": 2048,
                "validity": 100,
                "validity-type": "DAYS"
            }
        }
    }
    ```

5.  Choose *Create*.


<a name="task_qmb_srr_hsb"/>

<!-- task\_qmb\_srr\_hsb -->

## Creating Service Key for Cloud Foundry Application Document Management Service, Integration Option with X509 Certificate

Create service keys with X509 certificate using the following steps.



<a name="task_qmb_srr_hsb__steps_yb2_trr_hsb"/>

## Procedure

1.  Select an instance for which you want to create a service key.

2.  In the details area of the service instance, select the Actions menu \(<span class="SAP-icons"></span>\).

3.  Choose *Create Service Key*.

4.  In the *New Service Key* wizard, enter the *Service Key Name* and specify the following parameters in JSON format:

    ```json
    
    {
      "xsuaa": {
        "credential-type": "x509",
        "x509": {
          "key-length": 2048,
          "validity": 100,
          "validity-type": "DAYS"
        }
      }
    }
    ```

5.  Choose *Create*.




<a name="task_qmb_srr_hsb__result_gsk_qcs_hsb"/>

## Results

You can retrieve the access token with an X509 certificate. For detailed steps, see [Retrieving Tokens with mTLS](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/63fd9f1a140245df870dd7150ff15292.html?locale=en-US&version=Cloud).

