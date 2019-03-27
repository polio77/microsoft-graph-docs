
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var color = new CalendarColor
{
};

var calendars = new Calendar
{
	Name = "name-value",
	Color = color,
};

await graphClient.Me.CalendarGroups["{id}"].Calendars
	.Request()
	.AddAsync(calendars);

```