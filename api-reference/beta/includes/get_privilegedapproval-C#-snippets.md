
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var privilegedApproval = await graphClient.PrivilegedApproval
	.Request()
	.GetAsync();

```