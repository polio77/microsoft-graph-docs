
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var replies = await graphClient.Teams["{id}"].Channels["{id}"].Messages["{id}"].Replies
	.Request()
	.GetAsync();

```