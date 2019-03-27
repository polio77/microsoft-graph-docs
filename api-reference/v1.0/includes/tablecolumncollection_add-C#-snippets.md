
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var index = 3;

var values = new List<Int32>();

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Columns
	.add(index,values,name);
	.Request()
	.PostAsync()

```