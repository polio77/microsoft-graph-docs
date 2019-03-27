
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupIds = new List<String>();

await graphClient.ServicePrincipals["{id}"]
	.checkMemberGroups(groupIds);
	.Request()
	.PostAsync()

```