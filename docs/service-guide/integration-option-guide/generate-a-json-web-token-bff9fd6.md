<!-- loiobff9fd6addce47f3975442a768970d32 -->

# Generate a JSON Web Token

Use the parameters from your Document Management Service, Integration Option instance to generate a JSON Web Token \(JWT\) that serves as your authorization for making API calls.



## Procedure

1.  Navigate to the service key that you created.

    You would have directly created a service key or created one while binding the service instance to your application.

2.  Make a POST request to fetch a JWT using the parameters in the service key. The parameters for the POST request are:

    -   **URI**: <code><i class="varname">&lt;"uaa" : "url"&gt;</i>/oauth/token?grant_type=client_credentials</code>

    -   **HTTP Method**: *POST*

    -   **Authentication**: Basic

    -   **User name**: *<"uaa" : "clientId"\>*

    -   **Password**: *<"uaa" : "clientSecret"\>*


    In the response, you see the access token \(JWT\) that you need to make the onboarding API requests. For more information, see [Add Your Repository Using the Onboarding API](add-your-repository-using-the-onboarding-api-5fccabb.md).


