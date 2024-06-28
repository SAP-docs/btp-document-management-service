<!-- loio3fbbe2480b3c48f5b306af548a05ad8f -->

# App-to-App Integration of Document Management Service 

You can build URLs that perform actions in the SAP Document Management Service app and that can be used for app-to-app integration or as links in e-mails.

These URLs are either custom URLs \(`docmanagement://`\). In addition, there's a distinction between URLs for links for share members and URLs for public links, which can be accessed by anyone who receives the link \(and the password, if any\).



## App Support

**URL Type**


<table>
<tr>
<th valign="top">

URL Type

</th>
<th valign="top">

iOS App

</th>
<th valign="top">

Android App

</th>
<th valign="top">

Windows Desktop App

</th>
<th valign="top">

Mac Desktop App

</th>
</tr>
<tr>
<td valign="top">

Custom URL

</td>
<td valign="top" align="center">

x

</td>
<td valign="top" align="center">

x

</td>
<td valign="top" align="center">

x

</td>
<td valign="top" align="center">

x

</td>
</tr>
</table>

**Available Actions**


<table>
<tr>
<th valign="top">

Action

</th>
<th valign="top">

Comment

</th>
</tr>
<tr>
<td valign="top">

select

</td>
<td valign="top">

The folder containing the object identified with the parameter `obj` is opened and the object itself is selected in the documents list.

```
docmanagement://v1/select?rep=1234567890&obj=0987654321
```



</td>
</tr>
<tr>
<td valign="top">

open

</td>
<td valign="top">

-   If the parameter `obj` is the ID of a folder, the folder is opened and its content is displayed.
-   If the parameter `obj` is the ID of a file, the folder is opened and the file is downloaded.

```
docmanagement://v1/open?rep=1234567890&obj=0987654321
```



</td>
</tr>
</table>



## Available URL Parameters

-   *<rep\>* has the following values:

    -   *<repository ID\>*

    -   mydocuments

    -   share

    -   corporate


-   *<obj\>* has the following values:

    -   *<object ID\>*





## Custom URL Syntax

The custom URL syntax is:

```
docmanagement://<version>/<action>?parameters
```

> ### Example:  
> <code><code>docmanagement</code>://v1/open?obj=1234&amp;rep=abcdef</code>
> 
> This URL opens the document with the CMIS object ID `1234` from the SAP Document Management Service repository with ID `abcdef`, using version v1 of the SAP Document Management Service URL scheme and the `open` action.

The syntax contains the following elements:

-   `version` string, required

    Denotes the scheme version of SAP Document Management Service; the current version is v1.

-   `action` string, required: Is an action that the app performs on the provided parameters. Available actions are listed in the above mentioned table.

The syntax contains the following URL parameters:

-   `rep` string \(URL-encoded\), required

    SAP Document Management Service repository ID. If no object ID is provided or found, the repository root is selected.

-   `obj` string \(URL-encoded\), optional

    CMIS object ID of a file or folder.


**Related Information**  


[Working With the Mobile Apps \(Old\)](working-with-the-mobile-apps-old-c584be7.md "The various SAP Document Management Service applications (apps) need to be installed before you can use them on your devices.")

