
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var mentioned = new EmailAddress
{
	Name = "Dana Swope",
	Address = "danas@contoso.onmicrosoft.com",
};

var mentions = new List<Mention>();
mentions.Add(new Mention(mentioned));

var emailAddress = new EmailAddress
{
	Name = "Samantha Booth",
	Address = "samanthab@contoso.onmicrosoft.com",
};

var toRecipients = new List<Recipient>();
toRecipients.Add(new Recipient(emailAddress));

var messages = new Message
{
	Subject = "Party planning",
	ToRecipients = toRecipients,
	Mentions = mentions,
};

await graphClient.Me.Messages
	.Request()
	.AddAsync(messages);

```