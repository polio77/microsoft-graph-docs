
```C#

GraphServiceClient graphClient = new GraphServiceClient();

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Columns["{id|name}"]
	.dataBodyRange();
	.Request()
	.PostAsync()

```