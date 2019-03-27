
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var security = await graphClient.Security
	.Request()
	.GetAsync();

```