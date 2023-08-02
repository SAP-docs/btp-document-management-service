<!-- loioc91ec16e80804b91b0b05ea969ea2b87 -->

# Configurations for Reuse UI

Learn about the properties and aggregations of the reuse UI and make configuration changes as per your requirements.



## Properties

Add the properties while you declare the `componentUsage` to configure the reuse UI.


<table>
<tr>
<th valign="top">

Name



</th>
<th valign="top">

Required



</th>
<th valign="top">

Type



</th>
<th valign="top">

Default Value



</th>
<th valign="top">

Description



</th>
</tr>
<tr>
<td valign="top">

`repositoryId` 



</td>
<td valign="top">

Yes



</td>
<td valign="top">

string



</td>
<td valign="top">

empty



</td>
<td valign="top">

The ID of the repository that you want to connect.



</td>
</tr>
<tr>
<td valign="top">

`objectId` 



</td>
<td valign="top">

Yes



</td>
<td valign="top">

string



</td>
<td valign="top">

empty



</td>
<td valign="top">

The ID of the object \(folder/document\) that you want to load.



</td>
</tr>
<tr>
<td valign="top">

`destinationPath` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

string



</td>
<td valign="top">

*/comsapecmreuse.comsapecmreusedocumentTable/api* 



</td>
<td valign="top">

The path where Document Management Service, Integration Option's API is exposed; the path used in the approuter to route request to 'com.sap.ecm.reuse' service.



</td>
</tr>
<tr>
<td valign="top">

`homeFolderId` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

string



</td>
<td valign="top">

empty



</td>
<td valign="top">

The object ID of a folder assigned as the home/root folder for the Reuse UI, hence builds breadcrumbs accordingly. If not mentioned, ID of the repository's root folder is considered.



</td>
</tr>
<tr>
<td valign="top">

`homeFolderAlias` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

string



</td>
<td valign="top">

empty



</td>
<td valign="top">

The name of the home folder to show if the 'homeFolderId' property is defined.



</td>
</tr>
<tr>
<td valign="top">

`sortByCmisProperty` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

string



</td>
<td valign="top">

cmis:name



</td>
<td valign="top">

The CMIS property on which the reuse UI is to be sorted.



</td>
</tr>
<tr>
<td valign="top">

`sortAscending` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

boolean



</td>
<td valign="top">

true



</td>
<td valign="top">

If true, sorting is set to ascending. If false, sorting is set to descending. Can sort string, number, and date properties.



</td>
</tr>
<tr>
<td valign="top">

`forceLoad` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

boolean



</td>
<td valign="top">

true



</td>
<td valign="top">

Set to `true` if you want to automatically load the root folder of the first repository, if the repository corresponding to 'repositoryId' parameter isn’t found.



</td>
</tr>
<tr>
<td valign="top">

`showACLView` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

boolean



</td>
<td valign="top">

false



</td>
<td valign="top">

Set to `true` if you want to show an access control tab for a document, which allows you to modify permissions for the document.



</td>
</tr>
<tr>
<td valign="top">

`hideUrl` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

boolean



</td>
<td valign="top">

true



</td>
<td valign="top">

Set to `false` if you want to show web link URL in the document or folder properties. If your application supports navigation and routing, you can typically use it to display the weblink.



</td>
</tr>
<tr>
<td valign="top">

`usePagination` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

boolean



</td>
<td valign="top">

false



</td>
<td valign="top">

Set to `true` if you want to divide a large number of documents list into smaller discrete page in the view mode. By default, pagination is enabled. This setting shows the pagination switch in repositories with more than 100 documents. The purpose of switch is to allow users to choose whether to load all the documents or to paginate the result in a table.



</td>
</tr>
<tr>
<td valign="top">

`downloadWithContentStreamName` 



</td>
<td valign="top">

Optional



</td>
<td valign="top">

boolean



</td>
<td valign="top">

false



</td>
<td valign="top">

You can set it to `false` if you want the file to be downloaded with *cmis:name*. Documents are downloaded by default based on `ContentStreamFileName`.



</td>
</tr>
</table>



<a name="loioc91ec16e80804b91b0b05ea969ea2b87__section_z2m_mzb_hpb"/>

## Aggregations

An aggregation is a strong relation that also manages the lifecycle of the related control. It defines aggregations for your component. A control can only be assigned to one single aggregation, if it's assigned to a second aggregation, it's removed from the previous aggregation automatically.

Aggregations is used to hold arrays of controls.


<table>
<tr>
<th valign="top">

Name



</th>
<th valign="top">

Required



</th>
<th valign="top">

Type



</th>
<th valign="top">

Description



</th>
</tr>
<tr>
<td valign="top">

`rowAction`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

sap.ui.core.Control



</td>
<td valign="top">

It's a single aggregation and it can be used to add an additional column in the document management table. Multiple columns aren't allowed in a table; only one column is allowed.



</td>
</tr>
<tr>
<td valign="top">

`customActions`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

sap.ui.core.Control



</td>
<td valign="top">

It's multiple aggregations and it can be used to insert an additional UI control to the table header. Multiple controls can be passed as an array.

> ### Note:  
> If you add too many controls, the UI can become packed, so plan accordingly. If the size of the controls increases, the table header should still match.



</td>
</tr>
<tr>
<td valign="top">

`CustomPropertyTab`



</td>
<td valign="top">

Optional



</td>
<td valign="top">

sap.ui.core.Control



</td>
<td valign="top">

It's a single aggregation and it can be used to extend the UI in property view, and any UI controls can be added to this view. Just one such extension is allowed.



</td>
</tr>
</table>

