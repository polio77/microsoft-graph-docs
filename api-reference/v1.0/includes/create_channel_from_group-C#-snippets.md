
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var channels = new Channel
{
	DisplayName = "Architecture Discussion",
	Description = "This channel is where we debate all future architecture plans",
};

await graphClient.Teams["{id}"].Channels
	.Request()
	.AddAsync(channels);

```