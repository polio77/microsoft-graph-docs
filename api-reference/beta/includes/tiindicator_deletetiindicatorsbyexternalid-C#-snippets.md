
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = new List<String>();

await graphClient.Security.TiIndicators
	.deleteTiIndicatorsByExternalId(value);
	.Request()
	.PostAsync()

```