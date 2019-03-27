
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var receivers = new List<String>();

var sources = new List<String>();

var audioRoutingGroups = new AudioRoutingGroup
{
	Id = "oneToOne",
	RoutingMode = "oneToOne",
	Sources = sources,
	Receivers = receivers,
};

await graphClient.App.Calls["{id}"].AudioRoutingGroups
	.Request()
	.AddAsync(audioRoutingGroups);

```