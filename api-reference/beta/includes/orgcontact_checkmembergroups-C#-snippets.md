
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupIds = new List<String>();

await graphClient.Contacts["{id}"]
	.checkMemberGroups(groupIds);
	.Request()
	.PostAsync()

```