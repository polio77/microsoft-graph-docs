
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var rows = await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Rows["{index}"]
	.Request()
	.GetAsync();

```