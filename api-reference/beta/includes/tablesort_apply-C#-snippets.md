
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var icon = new WorkbookIcon
{
	Set = "set-value",
	Index = 99,
};

var dataOption = "dataOption-value";

var color = "color-value";

var ascending = True;

var sortOn = "sortOn-value";

var key = 99;

var fields = new List<WorkbookSortField>();
fields.Add(new WorkbookSortField(key));
fields.Add(new WorkbookSortField(sortOn));
fields.Add(new WorkbookSortField(ascending));
fields.Add(new WorkbookSortField(color));
fields.Add(new WorkbookSortField(dataOption));
fields.Add(new WorkbookSortField(icon));

var matchCase = True;

var method = "method-value";

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Sort
	.apply(fields,matchCase,method);
	.Request()
	.PostAsync()

```