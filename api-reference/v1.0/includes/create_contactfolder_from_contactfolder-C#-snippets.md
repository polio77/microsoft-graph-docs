
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var childFolders = new ContactFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.ContactFolders["{id}"].ChildFolders
	.Request()
	.AddAsync(childFolders);

```