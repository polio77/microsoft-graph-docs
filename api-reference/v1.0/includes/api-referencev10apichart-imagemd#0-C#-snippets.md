
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var image = await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Image(640, 480, 'fit')
	.Request()
	.GetAsync();

```