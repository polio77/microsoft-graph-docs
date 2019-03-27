
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var participants = new List<String>();

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"].Participants
	.muteAll(participants,clientContext);
	.Request()
	.PostAsync()

```