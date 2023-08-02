<!-- loio46e8aaa67a414e6c80b1d2884074faad -->

# Develop Using Client Credential Flow

Build document management capabilities using Document Management Service, Integration Option and CMIS APIs.



## Procedure

1.  Use the credentials of Document Management Service, Integration Option and make a POST request to fetch a JSON Web Token. The parameters for the POST request are:

    -   **URI**: <code><i class="varname">&lt;"uaa" : "url"&gt;</i>/oauth/token?grant_type=client_credentials</code>

    -   **HTTP Method**: *POST*

    -   **Authentication**: Basic

    -   **User name**: *<"uaa" : "clientId"\>*

    -   **Password**: *<"uaa" : "clientSecret"\>*


    The values that you pasSs on via `X-EcmUserEnc` and `X-EcmAddPrincipals` are propagated to the repository. If you don't send these parameters, Document Management Service, Integration Option populates the document properties *createdBy* and *modifiedBy* as *anonymous*.

    In the API response, you see the access token \(JWT\) that you need for the next step.

2.  Use CMIS client libraries or CMIS APIs to develop your own clients. See [Apache Chemistry](http://chemistry.apache.org/). To connect your repository to CMIS, use the browser end point from the object *<"endpoints": "ecmservice": "URL"\>* in the service key.

    Using this procedure until this point, creation of document or folder is propagated with the technical user ID. If you want to pass the logged in user ID \(from your business application\), follow the next step.

3.  To generate and propagate the same user token that you use in your business application to Document Management Service, Integration Option, see [UAA API Reference](https://docs.cloudfoundry.org/api/uaa/version/74.19.0/index.html#user-token-grant).


