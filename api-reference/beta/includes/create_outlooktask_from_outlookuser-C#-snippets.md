
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var dueDateTime = new DateTimeTimeZone
{
	DateTime = "2016-05-05T16:00:00",
	TimeZone = "Eastern Standard Time",
};

var startDateTime = new DateTimeTimeZone
{
	DateTime = "2016-05-03T09:00:00",
	TimeZone = "Eastern Standard Time",
};

var tasks = new OutlookTask
{
	AssignedTo = "Dana Swope",
	Subject = "Shop for children's weekend",
	StartDateTime = startDateTime,
	DueDateTime = dueDateTime,
};

await graphClient.Me.Outlook.Tasks
	.Request()
	.AddAsync(tasks);

```