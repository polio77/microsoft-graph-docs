
```C#

GraphServiceClient graphClient = new GraphServiceClient();

await graphClient.Education.SynchronizationProfiles["{id}"]
	.reset();
	.Request()
	.PostAsync()

```