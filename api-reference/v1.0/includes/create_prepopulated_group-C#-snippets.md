
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var members@odata.bind = new List<>();

var owners@odata.bind = new List<>();

var groupTypes = new List<String>();

var groups = new Group
{
	Description = "Group with designated owner and members",
	DisplayName = "Operations group",
	GroupTypes = groupTypes,
	MailEnabled = true,
	MailNickname = "operations2019",
	SecurityEnabled = false,
	Owners@odata.bind = owners@odata.bind,
	Members@odata.bind = members@odata.bind,
};

await graphClient.Groups
	.Request()
	.AddAsync(groups);

```