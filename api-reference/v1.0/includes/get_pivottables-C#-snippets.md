
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var pivotTables = await graphClient.Me.Drive.Root.Workbook.Worksheets["{id}"].PivotTables
	.Request()
	.GetAsync();

```