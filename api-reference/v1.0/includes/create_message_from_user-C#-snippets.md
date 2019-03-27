
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var emailAddress = new EmailAddress
{
	Address = "AdeleV@contoso.onmicrosoft.com",
};

var toRecipients = new List<Recipient>();
toRecipients.Add(new Recipient(emailAddress));

var body = new ItemBody
{
	ContentType = "HTML",
	Content = "They were <b>awesome</b>!",
};

var messages = new Message
{
	Subject = "Did you see last night's game?",
	Importance = "Low",
	Body = body,
	ToRecipients = toRecipients,
};

await graphClient.Me.Messages
	.Request()
	.AddAsync(messages);

```