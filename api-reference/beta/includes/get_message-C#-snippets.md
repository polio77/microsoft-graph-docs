
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var messages = await graphClient.Me.Messages["AAMkAGI1AAAoZCfHAAA="]
	.Request()
	.GetAsync();

```