
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryRoleTemplates = await graphClient.DirectoryRoleTemplates
	.Request()
	.GetAsync();

```