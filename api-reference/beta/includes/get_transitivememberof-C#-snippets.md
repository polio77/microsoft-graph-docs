
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var transitiveMemberOf = await graphClient.Me.TransitiveMemberOf
	.Request()
	.GetAsync();

```