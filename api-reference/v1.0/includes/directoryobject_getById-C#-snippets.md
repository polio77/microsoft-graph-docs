
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var ids = new List<String>();

var types = new List<String>();

await graphClient.DirectoryObjects
	.getByIds(ids,types);
	.Request()
	.PostAsync()

```