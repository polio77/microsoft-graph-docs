
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var messages = await graphClient.Me.Messages["AAMkADhMGAAA="]
	.Request()
	.GetAsync();

```