
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var progressTaskBoardFormat = await graphClient.Planner.Tasks["<id>"].ProgressTaskBoardFormat
	.Request()
	.GetAsync();

```