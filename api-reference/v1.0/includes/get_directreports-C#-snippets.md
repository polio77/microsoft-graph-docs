
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directReports = await graphClient.Me.DirectReports
	.Request()
	.GetAsync();

```