
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = new List<String>();

await graphClient.Security.TiIndicators
	.deleteTiIndicators(value);
	.Request()
	.PostAsync()

```