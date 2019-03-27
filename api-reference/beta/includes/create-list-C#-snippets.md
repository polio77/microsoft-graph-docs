
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var list = new ListInfo
{
	Template = "genericList",
};

var number = new NumberColumn
{
};

var name = "PageCount";

var text = new TextColumn
{
};

var name = "Author";

var columns = new List<ColumnDefinition>();
columns.Add(new ColumnDefinition(name));
columns.Add(new ColumnDefinition(text));
columns.Add(new ColumnDefinition(name));
columns.Add(new ColumnDefinition(number));

var lists = new List
{
	Name = "Books",
	Columns = columns,
	List = list,
};

await graphClient.Sites["{site-id}"].Lists
	.Request()
	.AddAsync(lists);

```