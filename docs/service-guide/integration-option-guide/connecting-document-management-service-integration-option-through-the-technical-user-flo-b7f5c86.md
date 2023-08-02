<!-- loiob7f5c862ae744e4aa442451ad8d71bdf -->

# Connecting Document Management Service, Integration Option Through the Technical User Flow

There are situations where leading applications are unable to use the login user flow and instead want to propagate user information to the Document Management Service by using the technical user flow.



It can be achieved with the header parameters of the Document Management Service.

**`X-EcmUserEnc`**

-   It's necessary to pass user information in this parameter.

-   User information in this field will be propagated to the document when it’s created or modified.


**`X-EcmAddPrincipals`**

-   The parameter can be used if the user needs to send additional principals along with the actual user.

-   Based on the permission assigned to the principals passed, the user can perform operations.


**`X-EcmAdmin`**

-   If the owner of the document must be different from the actual user, then this parameter needs to be set.

-   If this parameter isn't passed, the `X-EcmUserEnc` parameter value is set as the owner of the document.


The following parameters can be passed to Document Management Service in two ways:

-   Using a JWT token

    -   The above mentioned parameters must be passed while generating the JWT token.

    -   Add the following section to the JWT token while it's being generated:

        > ### Sample Code:  
        > ```
        > 
        > https://<authenticationurl>/oauth/token?grant_type=client_credentials&authorities={"az_attr":{"X-EcmUserEnc":"<user_info>","X-EcmAddPrincipals":"<additional principals>", >","X-EcmAdmin":"<additional info>" }}
        > ```


-   Using request header

    -   The user information can be propagated in every document management API request such as creating documents, deleting documents, etc.

    -   Pass the authorities as a header and the following details as value:

        > ### Sample Code:  
        > ```
        > az_attr":{"X-EcmUserEnc":"<user_info>","X-EcmAddPrincipals":"<additional principals>", >","X-EcmAdmin":"<additional info>" } 
        > ```



> ### Note:  
> -   If you want to add Access Control principals with email and group name, you can separate it out using a semicolon \(;\). For example, in the `X-ECMAddPrincipals:test@sap.com;~group~HiringManagers` principal semicolon \(;\) has been used as a delimiter when adding access control principals.
> 
> -   White spaces in the role collections are also supported. When there is only one group name with a space, the delimiter semicolon \(;\) must be used at the end of the principal.
> 
>     > ### Example:  
>     > `~group~Hiring Managers;`

