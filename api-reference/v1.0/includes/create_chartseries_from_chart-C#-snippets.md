
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var series = new WorkbookChartSeries
{
	Name = "name-value",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Series
	.Request()
	.AddAsync(series);

```