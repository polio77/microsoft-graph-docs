
```C#

GraphServiceClient graphClient = new GraphServiceClient();

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"]
	.convertToRange();
	.Request()
	.PostAsync()

```