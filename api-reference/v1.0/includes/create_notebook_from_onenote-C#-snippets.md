
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var notebooks = new Notebook
{
	DisplayName = "Notebook name",
};

await graphClient.Me.Onenote.Notebooks
	.Request()
	.AddAsync(notebooks);

```