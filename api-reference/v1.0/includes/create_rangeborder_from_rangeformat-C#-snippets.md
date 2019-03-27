
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var borders = new WorkbookRangeBorder
{
	Id = "id-value",
	Color = "color-value",
	Style = "style-value",
	SideIndex = "sideIndex-value",
	Weight = "weight-value",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
	.range();.Format.Borders
	.Request()
	.AddAsync(borders);

```