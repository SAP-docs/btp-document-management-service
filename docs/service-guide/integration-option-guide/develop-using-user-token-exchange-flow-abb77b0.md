<!-- loioabb77b0a1d5f4d39aafdc40c8483de1e -->

# Develop Using User Token Exchange Flow

Build document management capabilities using Document Management Service, Integration Option, CMIS APIs, and User Account and Authentication provided by Cloud Foundry.



## Procedure

1.  Make a POST request to fetch a JSON Web Token. The parameters for the POST request are:

    -   **URI**: <code><i class="varname">&lt;"uaa" : "url"&gt;</i>/oauth/token?grant_type=client_credentials</code>

    -   **HTTP Method**: *POST*

    -   **Authentication**: Basic

    -   **User name**: *<"uaa" : "clientId"\>*

    -   **Password**: *<"uaa" : "clientSecret"\>*


    In the API response, you see the access token \(JWT\) that you need for the next step.

2.  Connect to your repository by calling the browser end point using the CMIS workbench.

    You can identify the browser end point from the object *<"endpoints": "ecmservice": "browser end point URL"\>* in the service key.

3.  Use CMIS client libraries or CMIS APIs to develop your own clients. See [Apache Chemistry](http://chemistry.apache.org/).

4.  To generate and propagate the same user token that you use in your business application to Document Management Service, Integration Option, see [UAA API Reference](https://docs.cloudfoundry.org/api/uaa/version/74.19.0/index.html#user-token-grant).


