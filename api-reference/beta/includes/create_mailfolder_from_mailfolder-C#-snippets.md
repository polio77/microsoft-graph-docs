
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var childFolders = new MailFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.MailFolders["{id}"].ChildFolders
	.Request()
	.AddAsync(childFolders);

```