
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var parentReference = new String
{
	Path = "/drive/root:/Documents",
};

var name = "Copy of LargeFolder1";

await graphClient.Me.Drive.Items["{folder-item-id}"]
	.copy(name,parentReference);
	.Request()
	.PostAsync()

```