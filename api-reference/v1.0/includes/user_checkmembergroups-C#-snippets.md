
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupIds = new List<String>();

await graphClient.Me
	.checkMemberGroups(groupIds);
	.Request()
	.PostAsync()

```