
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var userIds = new List<String>();

var schedulingGroups = new SchedulingGroup
{
	DisplayName = "Cashiers",
	IsActive = true,
	UserIds = userIds,
};

await graphClient.Teams["{teamId}"].Schedule.SchedulingGroups
	.Request()
	.AddAsync(schedulingGroups);

```