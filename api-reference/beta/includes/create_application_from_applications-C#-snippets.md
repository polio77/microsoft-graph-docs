
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var applications = new Application
{
	AllowPublicClient = true,
	DisplayName = "Display name",
};

await graphClient.Applications
	.Request()
	.AddAsync(applications);

```