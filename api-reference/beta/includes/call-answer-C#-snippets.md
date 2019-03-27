
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var callbackUri = "callbackUri-value";

var mediaConfig = new String
{
	@odata.type = "#microsoft.graph.appHostedMediaConfig",
	Blob = "<media config blob>",
};

var acceptedModalities = new List<String>();

await graphClient.App.Calls["{id}"]
	.answer(callbackUri,mediaConfig,acceptedModalities);
	.Request()
	.PostAsync()

```