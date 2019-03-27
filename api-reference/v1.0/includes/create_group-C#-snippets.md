
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupTypes = new List<String>();

var groups = new Group
{
	Description = "Self help community for library",
	DisplayName = "Library Assist",
	GroupTypes = groupTypes,
	MailEnabled = true,
	MailNickname = "library",
	SecurityEnabled = false,
};

await graphClient.Groups
	.Request()
	.AddAsync(groups);

```