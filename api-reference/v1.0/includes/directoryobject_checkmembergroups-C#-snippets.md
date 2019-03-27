
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupIds = new List<String>();

await graphClient.DirectoryObjects["{id}"]
	.checkMemberGroups(groupIds);
	.Request()
	.PostAsync()

```