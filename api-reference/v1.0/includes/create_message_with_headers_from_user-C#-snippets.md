
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = "WA001";

var name = "x-custom-header-group-id";

var value = "Washington";

var name = "x-custom-header-group-name";

var internetMessageHeaders = new List<InternetMessageHeader>();
internetMessageHeaders.Add(new InternetMessageHeader(name));
internetMessageHeaders.Add(new InternetMessageHeader(value));
internetMessageHeaders.Add(new InternetMessageHeader(name));
internetMessageHeaders.Add(new InternetMessageHeader(value));

var emailAddress = new EmailAddress
{
	Address = "AlexW@contoso.OnMicrosoft.com",
};

var toRecipients = new List<Recipient>();
toRecipients.Add(new Recipient(emailAddress));

var body = new ItemBody
{
	ContentType = "HTML",
	Content = "The group represents Washington.",
};

var messages = new Message
{
	Subject = "9/8/2018: concert",
	Body = body,
	ToRecipients = toRecipients,
	InternetMessageHeaders = internetMessageHeaders,
};

await graphClient.Me.Messages
	.Request()
	.AddAsync(messages);

```