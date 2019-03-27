
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var domains = new Domain
{
	Id = "contoso.com",
};

await graphClient.Domains
	.Request()
	.AddAsync(domains);

```