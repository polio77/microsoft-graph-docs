
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var mailFolders = new MailFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.MailFolders
	.Request()
	.AddAsync(mailFolders);

```