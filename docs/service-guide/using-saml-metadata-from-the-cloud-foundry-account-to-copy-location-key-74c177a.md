<!-- loio74c177a3ba014a4c83bd1319a97fa9f3 -->

# Using SAML Metadata from the Cloud Foundry Account to Copy Location Key

Get the SAML service provider metadata from your Cloud Foundry account.



<a name="loio74c177a3ba014a4c83bd1319a97fa9f3__prereq_brs_jyp_stb"/>

## Prerequisites

You're a Cloud Foundry administrator.



## Procedure

1.  Log on to your SAP BTP cockpit and navigate to your subaccount.

2.  Choose *Security* \> *Trust Configuration*.

3.  Choose *SAML Metadata*.

4.  Specify a file name and save the metadata locally on your computer.

5.  Navigate to the file in your Explorer and right-click on it. Then open the file with any editor.

6.  Scroll down to the bottom of the file to find the token endpoint.

    > ### Example:  
    > Find the key [Location\] `https://abc-de.authentication.sap.hana.ondemand.com/oauth/token/alias/abc-de.test`

7.  Copy the URL and store it.


