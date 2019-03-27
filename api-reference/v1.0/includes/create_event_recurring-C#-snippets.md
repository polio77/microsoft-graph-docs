
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var type = "required";

var emailAddress = new 
{
	Address = "AdeleV@contoso.onmicrosoft.com",
	Name = "Adele Vance",
};

var attendees = new List<Attendee>();
attendees.Add(new Attendee(emailAddress));
attendees.Add(new Attendee(type));

var location = new Location
{
	DisplayName = "Harry's Bar",
};

var range = new RecurrenceRange
{
	Type = "endDate",
	StartDate = "2017-09-04",
	EndDate = "2017-12-31",
};

var daysOfWeek = new List<DayOfWeek>();

var pattern = new RecurrencePattern
{
	Type = "weekly",
	Interval = 1,
	DaysOfWeek = daysOfWeek,
};

var recurrence = new PatternedRecurrence
{
	Pattern = pattern,
	Range = range,
};

var end = new DateTimeTimeZone
{
	DateTime = "2017-09-04T14:00:00",
	TimeZone = "Pacific Standard Time",
};

var start = new DateTimeTimeZone
{
	DateTime = "2017-09-04T12:00:00",
	TimeZone = "Pacific Standard Time",
};

var body = new ItemBody
{
	ContentType = "HTML",
	Content = "Does noon time work for you?",
};

var events = new Event
{
	Subject = "Let's go for lunch",
	Body = body,
	Start = start,
	End = end,
	Recurrence = recurrence,
	Location = location,
	Attendees = attendees,
};

await graphClient.Me.Events
	.Request()
	.AddAsync(events);

```