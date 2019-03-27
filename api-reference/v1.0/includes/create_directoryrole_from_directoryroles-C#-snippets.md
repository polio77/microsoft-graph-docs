
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryRoles = new DirectoryRole
{
	RoleTemplateId = "roleTemplateId-value",
};

await graphClient.DirectoryRoles
	.Request()
	.AddAsync(directoryRoles);

```