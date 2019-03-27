
```C#

GraphServiceClient graphClient = new GraphServiceClient();

await graphClient.Education.SynchronizationProfiles["{id}"]
	.pause();
	.Request()
	.PostAsync()

```