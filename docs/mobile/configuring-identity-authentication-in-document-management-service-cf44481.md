<!-- loiocf44481aa6184786a8bb600c4a2afacf -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Configuring Identity Authentication In Document Management Service

An SAP Business Technology Platform Identity Authentication Service \(IAS\) is required to authenticate with SAP Document Management Service desktop application for Microsoft Windows and Mac OS.



<a name="loiocf44481aa6184786a8bb600c4a2afacf__prereq_akv_m4g_3rb"/>

## Prerequisites

You've created an IAS tenant.

> ### Remember:  
> You need to order your own SAP Cloud Identity instance and manage your users in your own SAP Cloud Identity instance. Contact your account executive to get an account. For more information, see [Tenant Model and Licensing](https://help.sap.com/viewer/6d6d63354d1242d185ab4830fc04feb1/Cloud/en-US/93160ebd2dcb40e98aadcbb9a970f2b9.html).



## Procedure

1.  In the SAP BTP cockpit, go to your subaccount.

2.  Choose *Security* \> *Trust Configuration.*

3.  Choose *Establish Trust*.

    > ### Note:  
    > If the *Establish Trust* button is disabled, trust has already been established, and this step can be skipped.

4.  In the following popup, select an identity provider from the dropdown list.

    Only identity providers that are associated with your customer ID are shown.

5.  Choose *Establish Trust*.




<a name="loiocf44481aa6184786a8bb600c4a2afacf__result_s4p_czg_3rb"/>

## Results

You've configured trust in your tenant of the Identity Authentication service, which is your identity provider. Identity Authentication creates an application with the prefix *XSUAA\_* and the display name of your subaccount in the Administration console for Identity Authentication.

> ### Example:  
> If your subaccount was named *My Subaccount*, the resulting application in Identity Authentication would be *XSUAA\_My Subaccount*.

<a name="task_c4b_b1h_3rb"/>

<!-- task\_c4b\_b1h\_3rb -->

## Creating Service Instance for Identity Authentication

Create service instances for Identity Authentication tenants from your subaccount.



<a name="task_c4b_b1h_3rb__prereq_nvb_r2h_3rb"/>

## Prerequisites

If you’re working in an enterprise account, you need to add quotas to the Identity Authentication services you purchased in your subaccount before they appear in the service marketplace. Otherwise, only default free-of-charge services are listed. Quotas are automatically assigned to the resources available in free accounts.

For more information, see [Configure Entitlements and Quotas for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html?q=Configure%20entitlements%20and%20quotas%20for%20subaccounts).



<a name="task_c4b_b1h_3rb__steps_wrp_kdh_3rb"/>

## Procedure

1.  In the SAP BTP cockpit, navigate to the subaccount in which you want to create a service instance.

2.  In the navigation area, choose *Services* \> *Instances and Subscriptions*.

3.  Select *Create* in the top-right corner. A wizard opens, offering you to configure your new instance.

4.  Choose a service for which you wish to create an instance from the dropdown list.

5.  Select one of the available service plans.

6.  Choose *Cloud Foundry* as a runtime environment.

7.  Select a space in your Cloud Foundry org to create the instance.

8.  Enter a name for your service instance, then choose *Next*.

9.  Under *Configure instance parameters*, specify a JSON file to upload or configure parameters manually in the JSON format, then choose *Next*.

    > ### Sample Code:  
    > ```json
    > 
    > {
    >   "oauth2-configuration":
    >   {
    >     "post-logout-redirect-uris": ["https://*.cfapps.sap.hana.ondemand.com/*/logout.html"],
    >     "redirect-uris": [
    >       "https://*.cfapps.sap.hana.ondemand.com/login/callback?authType=ias",
    >       "https://oauth.docmanagement.io/v1/callback"]
    >   },
    >   "public-client": true,
    >   "xsuaa-cross-consumption": true,
    >   "multi-tenant": false
    > }
    > ```

10. Use the preview to verify the instance details, then choose *Create*.

    The new instance of the SAP Cloud Identity service is created in your Cloud Foundry space.

11. Create a *Service Key* for the SAP Cloud Identity service. For more information, see [Reference Information for the Identity Service of SAP BTP](https://help.sap.com/docs/IDENTITY_AUTHENTICATION/6d6d63354d1242d185ab4830fc04feb1/9379444abf3f4e2cbaade7c4001df381.html?locale=en-US&version=Cloud).


<a name="task_cs2_2hh_3rb"/>

<!-- task\_cs2\_2hh\_3rb -->

## Create and Consume a Destination for the Identity Authentication Service



<a name="task_cs2_2hh_3rb__prereq_m3y_blh_3rb"/>

## Prerequisites

You've enabled the *Public* client type, for the newly created application. In the Administration console, choose the *OpenID connect application* \> *Client ID, Secrets and Certificates*. Under the *Trust* tab, enable *Public* under *Client Type*.



<a name="task_cs2_2hh_3rb__steps_tyr_nmh_3rb"/>

## Procedure

1.  In the SAP BTP cockpit, navigate to your Cloud Foundry subaccount and from the left-side subaccount menu, choose *Connectivity* \> *Destinations*.

2.  Choose *New Destination*.

3.  Then provide the following settings:


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    Details
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    **Name**
    
    </td>
    <td valign="top">
    
    Insert the client name as `SDM_Mobile_Client`

    > ### Note:  
    > The destination name is hardcoded as we don't accept any other destination names.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    **Type**
    
    </td>
    <td valign="top">
    
    `HTTP`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    **Description**
    
    </td>
    <td valign="top">
    
    *<Any Description\>*
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    **URL**
    
    </td>
    <td valign="top">
    
    URL of the Identity Authentication that you want to consume.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    **Proxy Type**
    
    </td>
    <td valign="top">
    
    `Internet`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    **Authentication**
    
    </td>
    <td valign="top">
    
    `OAuth2UserTokenExchange`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    **Client ID**
    
    </td>
    <td valign="top">
    
    Copy the `clientID` from *Client ID, Secrets, and Certificates* section of the Identity Authentication application.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    **Client Secret**
    
    </td>
    <td valign="top">
    
    Copy the `clientsecret` from the service key created for the Identity Authentication application.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    **Token Service URL Type**
    
    </td>
    <td valign="top">
    
    Select *Dedicated*.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    **Token Service URL**
    
    </td>
    <td valign="top">
    
    `<Identity Authentication Tenant URL>/oauth2/token`
    
    </td>
    </tr>
    </table>
    

<a name="task_k1z_yrh_3rb"/>

<!-- task\_k1z\_yrh\_3rb -->

## Assigning Role Collections to Users

Assign a role collection to a business user.



<a name="task_k1z_yrh_3rb__steps_q4z_hsh_3rb"/>

## Procedure

1.  In the SAP BTP cockpit, navigate to your subaccount.

2.  Choose *Security* \> *Role Collections*.

3.  To create a new role collection, choose :heavy_plus_sign: \(Create New Role Collection\). To copy an existing role collection, choose *Copy* at the end of the row.

4.  Enter a new name and description. If you copied an existing role collection, you can see the included roles.

5.  Save your changes.

6.  To add roles, choose the role collection name.

7.  Go to the *Roles* section and choose *Edit*.

8.  To add a role to the role collection, choose the input field. The role selection screen opens. Choose `SDM_User` and `SDM_Admin` roles.

9.  Choose *Add*.

10. Go to the *Users* section. Enter the user ID of the user that you want to assign to the role collection.

11. Choose the *Identity Provider* as `Custom IAS Tenant` and type in the email address.

12. Save your changes.


<a name="task_jcl_y13_3rb"/>

<!-- task\_jcl\_y13\_3rb -->

## Creating SAP Document Management Service Destination



<a name="task_jcl_y13_3rb__prereq_lxk_5rt_d5b"/>

## Prerequisites

You've created a *Service Instance* and *Service Key* for Document Management Service, Integration Option. For more information, see [Creating a Service Instance and Service Key](https://help.sap.com/viewer/8e5c8dd3350245848edf216bf176444c/Dev/en-US/fe7f1e57e875429f90141b25d6d1dd64.html "Create an instance of Document Management Service, Integration Option.") :arrow_upper_right:.



<a name="task_jcl_y13_3rb__steps_hvb_kb3_3rb"/>

## Procedure

1.  In the SAP BTP cockpit, navigate to your Cloud Foundry subaccount and from the left-side subaccount menu, choose *Connectivity* \> *Destinations*.

2.  Choose *New Destination* \> *Service Instance*.

3.  In the drop-down list, select the *Service Instance* you created.

4.  Enter hard-coded name `SDM_Instance_Client` as it's.

    > ### Note:  
    > The destination name is hardcoded as we don't accept any other destination names.

5.  Choose *Next* \> *Save*.


<a name="task_sts_jc3_3rb"/>

<!-- task\_sts\_jc3\_3rb -->

## Onboarding Repository and Downloading Document Management Service Mobile Client

Use the following steps to onboard Document Management Service, Integration Option repositories.



<a name="task_sts_jc3_3rb__steps_zkf_zc3_3rb"/>

## Procedure

1.  Using the admin portal, onboard the repository and update *<SDM\_Instance\_Client\>* as the service instance field. For more information, See [Onboarding Internal Repository](https://help.sap.com/viewer/8e5c8dd3350245848edf216bf176444c/Dev/en-US/59e3cb769e4f4487a2417d59d65f8276.html "Connect your Document Management Service, Application Option to Document Management Service, Repository Option for file storage.") :arrow_upper_right:.

2.  Download Document Management Service Mobile client. Enter the following format in the serverUrl and Document Management Service, Integration Option API URL:

    > ### Sample Code:  
    > ```
    > <ecmserviceurl>/browser?subdomain=<Subaccount's Subdomain name>
    > ```

    > ### Example:  
    > `https://api-doc-my-test.cfapps.sap.hana.ondemand.com/browser?subdomain=mytestclient` 


