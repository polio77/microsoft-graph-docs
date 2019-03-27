
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var responseStatus = new ResponseStatus
{
	Response = "",
	Time = "datetime-value",
};

var events = new Event
{
	OriginalStartTimeZone = "originalStartTimeZone-value",
	OriginalEndTimeZone = "originalEndTimeZone-value",
	ResponseStatus = responseStatus,
	ICalUId = "iCalUId-value",
	ReminderMinutesBeforeStart = 99,
	IsReminderOn = true,
};

await graphClient.Groups["{id}"].Events
	.Request()
	.AddAsync(events);

```