
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var contactFolders = new ContactFolder
{
	ParentFolderId = "parentFolderId-value",
	DisplayName = "displayName-value",
};

await graphClient.Me.ContactFolders
	.Request()
	.AddAsync(contactFolders);

```