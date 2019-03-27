
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var jobs = new SynchronizationJob
{
	TemplateId = "BoxOutDelta",
};

await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs
	.Request()
	.AddAsync(jobs);

```