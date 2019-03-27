
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupTypes = new List<String>();

var groups = new Group
{
	Description = "Self help community for golf",
	DisplayName = "Golf Assist",
	GroupTypes = groupTypes,
	MailEnabled = true,
	MailNickname = "golfassist",
	SecurityEnabled = false,
};

await graphClient.Groups
	.Request()
	.AddAsync(groups);

```