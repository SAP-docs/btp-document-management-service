<!-- loio5d4b802267d14df2ab3b64b304945ead -->

# Repository Information

Consumers can use the CMIS repository information to connect to their choice of repository.

For each repository, the server provides repository information \(`RepositoryInfo`\) that describes a repository's general information and its capabilities. When an app calls a binding service URL without parameters, it gets a list of `RepositoryInfo` objects, one for every repository that is connected to Document Management Service, Integration Option. Apps can then use the repository ID and the provided navigation information to connect to one of the repositories.

For more information, see the OASIS Web page for `getRepositoryInfo`.

If you send a GET request to the service URL for AtomPub \(/mcm/atom\), you get the service document XML, which contains service definitions and a list of repositories. If you send a GET request to the service URL of the browser binding \(/mcm/json\), the server responds with a JSON representation of a list of `RepositoryInfo` objects.

> ### Example:  
> Getting the list of `RepositoryInfo` objects with OpenCMIS
> 
> ```
> 
> SessionFactory sessionFactory = SessionFactoryImpl.newInstance();
> Map parameter = new HashMap();
> parameter.put(SessionParameter.USER, "admin");
> parameter.put(SessionParameter.PASSWORD, "admin");
> parameter.put(SessionParameter.BROWSER_URL, server+"/browser");
> parameter.put(SessionParameter.BINDING_TYPE, BindingType.BROWSER.value());
> List<Repository> repositories = sessionFactory.getRepositories(parameters);
> 
> ```

For examples of basic operations such as reading, creating, updating, and deleting objects and folder navigation with OpenCMIS, see the *OpenCMIS Client API Developer's Guide*.

**Related Information**  


[getRepositoryInfo on OASIS Web page](http://docs.oasis-open.org/cmis/CMIS/v1.1/os/CMIS-v1.1-os.html#x1-1710002)

[OpenCMIS Client API Developer's Guide](http://chemistry.apache.org/java/developing/guide.html)

