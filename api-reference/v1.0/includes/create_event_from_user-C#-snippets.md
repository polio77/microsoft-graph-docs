
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var type = "required";

var emailAddress = new 
{
	Address = "samanthab@contoso.onmicrosoft.com",
	Name = "Samantha Booth",
};

var attendees = new List<Attendee>();
attendees.Add(new Attendee(emailAddress));
attendees.Add(new Attendee(type));

var location = new Location
{
	DisplayName = "Harry's Bar",
};

var end = new DateTimeTimeZone
{
	DateTime = "2017-04-15T14:00:00",
	TimeZone = "Pacific Standard Time",
};

var start = new DateTimeTimeZone
{
	DateTime = "2017-04-15T12:00:00",
	TimeZone = "Pacific Standard Time",
};

var body = new ItemBody
{
	ContentType = "HTML",
	Content = "Does late morning work for you?",
};

var events = new Event
{
	Subject = "Let's go for lunch",
	Body = body,
	Start = start,
	End = end,
	Location = location,
	Attendees = attendees,
};

await graphClient.Me.Events
	.Request()
	.AddAsync(events);

```