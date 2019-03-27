
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var sourceFolderIDs = new List<>();

var childFolders = new MailFolder
{
	@odata.type = "microsoft.graph.mailSearchFolder",
	DisplayName = "Get MyAnalytics",
	IncludeNestedFolders = true,
	SourceFolderIDs = sourceFolderIDs,
	FilterQuery = "contains(subject, 'MyAnalytics')",
};

await graphClient.Me.MailFolders["searchfolders"].ChildFolders
	.Request()
	.AddAsync(childFolders);

```