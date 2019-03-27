
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var borders = await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"].Range().Format.Borders["{sideIndex}"]
	.Request()
	.GetAsync();

```