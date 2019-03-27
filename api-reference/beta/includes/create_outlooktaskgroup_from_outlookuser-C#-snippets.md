
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var taskGroups = new OutlookTaskGroup
{
	Name = "Leisure tasks",
};

await graphClient.Me.Outlook.TaskGroups
	.Request()
	.AddAsync(taskGroups);

```