
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var taskFolders = new OutlookTaskFolder
{
	Name = "Volunteer",
};

await graphClient.Me.Outlook.TaskFolders
	.Request()
	.AddAsync(taskFolders);

```