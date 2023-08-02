<!-- loiod2459a33a6534ae4bda112b88e6c3a66 -->

# Know Your Usage

As an admin, you can measure the consumption made by your subaccounts.



<a name="loiod2459a33a6534ae4bda112b88e6c3a66__section_kjj_vlb_wcb"/>

## Measure API Calls Consumption



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/usage/api</code>

**HTTP Method:***GET*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\)



### Request Example

```


GET https://<"endpoints" : "ecmservice" : "url">/rest/v2/usage/api



```



### Response Example

A sample success response for the GET request that returns the number of API calls made by the service instance. By default, you see the API calls that are made in the current month by each tenant that consumes the service instance.

```

{
    "usageListOfTenants": [
        {
            "metrics": "API",
            "month": 9,
            "numberOfConsumers": 4,
            "perTenantApiUsageList": [
                {
                    "tenantId": "a09cf54f-****-****-****-86ee8d5d0588",
                    "tenantSubDomain": "my-subaccount-procurement-team",
                    "units": "number of api calls",
                    "usage": 2574
                },
                {
                    "tenantId": "aa9c97c7-****-****-****-0baad78e6ed5",
                    "tenantSubDomain": "my-org-subaccount-sales-team",
                    "units": "number of api calls",
                    "usage": 3766
                },
                {
                    "tenantId": "1c3c15c2-****-****-****-1063f7ee8324",
                    "tenantSubDomain": "my-org-subaccount-crm-team",
                    "units": "number of api calls",
                    "usage": 685
                },
                {
                    "tenantId": "6b85fdc2-****-****-****-7847704039ac",
                    "tenantSubDomain": "my-org-subaccount-s4-team",
                    "units": "number of api calls",
                    "usage": 3187
                }
            ],
            "serviceInstanceId": "b63114db-8cd0-4a5e-bc47-e753d25a58b6",
            "year": 2020
        }
    ]
}

```



<a name="loiod2459a33a6534ae4bda112b88e6c3a66__section_adc_gfl_wmb"/>

## Measure Storage Consumption



### Request

**URI:**<code><i class="varname">&lt;"endpoints" : "ecmservice" : "url"&gt;</i>/rest/v2/usage/storage</code>

**HTTP Method:***GET*

**Permissions:** Admin for Document Management Service, Integration Option via the scope `SDM_Admin`

**Authentication:** Bearer JWT \(token from [Generate a JSON Web Token](generate-a-json-web-token-bff9fd6.md)\)



### Request Example

```


GET https://<"endpoints" : "ecmservice" : "url">/rest/v2/usage/storage



```



### Response Example

A sample success response for the GET request that returns the bytes that are consumed by the service instance. By default, you see the bytes consumed by each repository of the consuming tenants of the service instance, in the current month.

```


  {
    "usageListOfTenants": [
        {
            "metrics": "storage",
            "month": 9,
            "numberOfConsumers": 4,
            "perTenantStorageUsageList": [
                {
                    "numberOfRepositories": 1,
                    "storageUsagePerRepository": {
                        "metrics": "Bytes",
                        "repositoryId": "55f9183a-****-****-****-142a00784eac",
                        "repositoryName": "procurement",
                        "usage": 2307097088
                    },
                    "tenantId": "a09cf54f-****-****-****-86ee8d5d0588",
                    "tenantSubDomain": "my-subaccount-procurement-team"
                },
                {
                    "numberOfRepositories": 1,
                    "storageUsagePerRepository": {
                        "metrics": "Bytes",
                        "repositoryId": "bb8929d3-****-****-****-0cede3a87879",
                        "repositoryName": "sales",
                        "usage": 155648
                    },
                    "tenantId": "aa9c97c7-****-****-****-0baad78e6ed5",
                    "tenantSubDomain": "my-subaccount-sales-team"
                },
                {
                    "numberOfRepositories": 2,
                    "storageUsagePerRepository": [
                        {
                            "metrics": "Bytes",
                            "repositoryId": "bfa4c644-****-****-****-05828c7c5350",
                            "repositoryName": "liteTest",
                            "usage": 155648
                        },
                        {
                            "metrics": "Bytes",
                            "repositoryId": "da832413-****-****-****-461d868e47fe",
                            "repositoryName": "freeTest",
                            "usage": 165356765184
                        }
                    ],
                    "tenantId": "1c3c15c2-****-****-****-1063f7ee8324",
                    "tenantSubDomain": "my-org-subaccount-crm-team"
                },
                {
                    "numberOfRepositories": 2,
                    "storageUsagePerRepository": [
                        {
                            "metrics": "Bytes",
                            "repositoryId": "69485e21-****-****-****-42419f90cdbf",
                            "repositoryName": "test",
                            "usage": 155648
                        },
                        {
                            "metrics": "Bytes",
                            "repositoryId": "13addc5e-****-****-****-3a69d0adb98d",
                            "repositoryName": "internal",
                            "usage": 110400760219
                        }
                    ],
                    "tenantId": "6b85fdc2-****-****-****-7847704039ac",
                    "tenantSubDomain": "my-org-subaccount-s4-team"
                }
            ],
            "year": 2020
        }
    ]
}


```

**Related Information**  


[Service Plan for Document Management](https://discovery-center.cloud.sap/serviceCatalog/document-management-integration-option)

