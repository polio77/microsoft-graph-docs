
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var calendars = new Calendar
{
	Name = "Volunteer",
};

await graphClient.Me.Calendars
	.Request()
	.AddAsync(calendars);

```