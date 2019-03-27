
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupIds = new List<String>();

await graphClient.Groups["{id}"]
	.checkMemberGroups(groupIds);
	.Request()
	.PostAsync()

```