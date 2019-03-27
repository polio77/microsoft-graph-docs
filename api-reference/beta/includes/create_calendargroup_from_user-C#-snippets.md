
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var calendarGroups = new CalendarGroup
{
	Name = "name-value",
	ClassId = "classId-value",
	ChangeKey = "changeKey-value",
};

await graphClient.Me.CalendarGroups
	.Request()
	.AddAsync(calendarGroups);

```