
```C#

GraphServiceClient graphClient = new GraphServiceClient();

await graphClient.Drives["{drive-id}"].Items["{item-id}"].Versions["{version-id}"]
	.restoreVersion();
	.Request()
	.PostAsync()

```