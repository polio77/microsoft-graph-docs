
```C#

GraphServiceClient graphClient = new GraphServiceClient();

await graphClient.Drive.Root.Workbook.Worksheets["{id}"]
	.range();
	.rowsAbove(count);
	.Request()
	.PostAsync()

```