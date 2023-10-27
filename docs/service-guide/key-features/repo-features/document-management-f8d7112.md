<!-- loiof8d711288bc54a1b89e225987f01c326 -->

<link rel="stylesheet" type="text/css" href="../../css/sap-icons.css"/>

# Document Management

The following document management features are included in the Document Management Service.

**Basic Document Management Capabilities**


<table>
<tr>
<th valign="top">

Features

</th>
<th valign="top">

Document Management Service, Integration Option

</th>
<th valign="top">

Document Management Service, Application Option

</th>
<th valign="top">

Additional Details

</th>
</tr>
<tr>
<td valign="top">

*Upload Document*

</td>
<td valign="top">

[SAP Business Accelerator Hub](https://api.sap.com/api/CreateDocumentApi/overview)

</td>
<td valign="top">

*Select Repository* \> *Create* \> *Document* \> *Upload File*

</td>
<td valign="top">

Virus scanning is supported only up to 400 MB for the Document Management Service, Repository Option. Beyond 400 MB, it'sn't supported.

</td>
</tr>
<tr>
<td valign="top">

*Rename Document*

</td>
<td valign="top">

[SAP Business Accelerator Hub](https://api.sap.com/api/UpdateFolder_Document_LinkApi/overview)

</td>
<td valign="top">

*Select File \>* Choose <span class="SAP-icons"></span> More Options *\> Rename* *\> Enter New Name* 

</td>
<td valign="top">

-   The property to be updated is `cmis:name` 

-   In versioned repositories, check out the document, rename, and check in.



</td>
</tr>
<tr>
<td valign="top">

*View Document Properties*

</td>
<td valign="top">

[SAP Business Accelerator Hub](https://api.sap.com/api/GetObjectApi/overview)

</td>
<td valign="top">

Select *Repository* \> *Document*, choose<span class="SAP-icons"></span> More Options and select *Show Properties*

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

*Move Folder*

</td>
<td valign="top">

[SAP Business Accelerator Hub](https://api.sap.com/api/UpdateFolder_Document_LinkApi/overview)

</td>
<td valign="top">

*Select Repository* \> *Select Folder* \> *Move*.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

*Copy Document*

</td>
<td valign="top">

[SAP Business Accelerator Hub](https://api.sap.com/api/CreateDocumentFromSourceApi/resource)

</td>
<td valign="top">

Select *Repository* \> *Choose File* \> *Copy*.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

*Move Document*

</td>
<td valign="top">

[SAP Business Accelerator Hub](https://api.sap.com/api/GetPropertiesApi/overview)

</td>
<td valign="top">

Select *Repository* \> ** \> *Document* \> *Move*

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

*Status Management*

</td>
<td valign="top">

\(Not Applicable\)

</td>
<td valign="top">

Select *Repository* \> *Document*, choose <span class="SAP-icons"></span> More Options and select *Show Properties* *\> Edit \> Additional Data*

</td>
<td valign="top">

For SAP S/4HANA DMS repositories only.

</td>
</tr>
<tr>
<td valign="top">

*Classification*

</td>
<td valign="top">

\(Not Applicable\)

</td>
<td valign="top">

Select *Repository* \> *Document* Choose <span class="SAP-icons"></span> More Options*\> Show Properties* *\> Edit \> Additional Data*

</td>
<td valign="top">

For SAP S/4HANA DMS repositories only.

</td>
</tr>
<tr>
<td valign="top">

*Rendition Capabilities*

</td>
<td valign="top">

\(Not Applicable\)

</td>
<td valign="top">

Select *Repository* \> *Document* Choose <span class="SAP-icons"></span> More Options *\> Show Properties* *\> Edit \> Additional Data*

</td>
<td valign="top">

For SAP S/4HANA DMS repositories only.

</td>
</tr>
<tr>
<td valign="top">

*Download Content*

</td>
<td valign="top">

[SAP Business Accelerator Hub](https://api.sap.com/api/GetZipContentStream/overview)

</td>
<td valign="top">

Select *Repository*, choose *Document*, and then choose *Download*.

> ### Tip:  
> The *Download* option allows you to select multiple documents.



</td>
<td valign="top">

 

</td>
</tr>
</table>

