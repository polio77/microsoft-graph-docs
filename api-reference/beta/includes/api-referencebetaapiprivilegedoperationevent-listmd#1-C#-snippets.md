
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var privilegedOperationEvents = await graphClient.PrivilegedOperationEvents
	.Request()
	.Filter("requestType eq 'Activate'")
	.GetAsync();

```