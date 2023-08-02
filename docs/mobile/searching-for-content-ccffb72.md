<!-- loioccffb7206136447ba2b9c8047144e8a4 -->

# Searching for Content

This function of the SAP Document CenterSAP Mobile Documents Web app enables you to search for content by keywords in any repository, and browse the search results quickly and easily.



## Prerequisites

Your repositories are indexed in the CMS back-end systems.



## Context

You can search for content in the repository by using the *Search* field next to the *Sorting* field.

If you want to use wild cards, it is good to know that \*, ?, %, and \_ are treated as characters only. Double quotes \("\) can be used to start and end phrases. If your input contains an uneven number of double quotes, a trailing double quote is assumed.

> ### Note:  
> -   You cannot use the search to find folders.
> -   Some searches are case sensitive.
> -   Search results can vary depending on your back-end system \(which could be Knowledge Management, Document Service, Microsoft SharePoint, or Alfresco\) even if the keywords are the same, since there are special query rules for the respective repositories.
> 
>     > ### Example:  
>     > -   Knowledge Management without TREX search enabled: The search result list will consist of files that contain the search term in their name and description.
>     > -   Document Service: The search is case insensitive and the search result list will consist of files that contain the search term in their name and content.
>     > -   Microsoft SharePoint with full-text search enabled: The search will include all items in the whole repository and not just the current folder and its sub-folders.
>     > -   Microsoft SharePoint without full-text search enabled: Searches for the exact name, which means that the search is case-sensitive and complete. If you enter two search terms, you will get no result at all.
>     > -   Alfresco: If your search term contains \*, it will be considered as a wild card.



## Procedure

1.  Insert the keywords in the *Search* field and choose *Enter* or click the magnifier.

    The search results are displayed as a plain list of files that contain the keywords you entered in the *Search* field in their file name, content, or description.

    Also, if your back-end system is Knowledge Management, a content snippet is shown next to each item of the search result list.

2.  Navigate to a folder from the search list to see the content of this folder.

    > ### Note:  
    > The displayed results might not show the latest documents if these were uploaded after you navigated away from the results list.

3.  Click the browser back button or use the breadcrumbs to go to the root folder from where you started the search.


