
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var user = new Identity
{
	Id = "550fae72-d251-43ec-868c-373732c2704f",
};

var identity = new IdentitySet
{
	User = user,
};

var organizer = new MeetingParticipantInfo
{
	Identity = identity,
};

var participants = new MeetingParticipants
{
	Organizer = organizer,
};

var onlineMeetings = new OnlineMeeting
{
	MeetingType = "meetNow",
	Participants = participants,
	Subject = "subject-value",
};

await graphClient.App.OnlineMeetings
	.Request()
	.AddAsync(onlineMeetings);

```