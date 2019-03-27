
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var emailAddress = new EmailAddress
{
	Address = "danas@contoso.onmicrosoft.com",
};

var ccRecipients = new List<Recipient>();
ccRecipients.Add(new Recipient(emailAddress));

var emailAddress = new EmailAddress
{
	Address = "samanthab@contoso.onmicrosoft.com",
};

var toRecipients = new List<Recipient>();
toRecipients.Add(new Recipient(emailAddress));

var body = new ItemBody
{
	ContentType = "Text",
	Content = "The new cafeteria is open.",
};

var message = new Message
{
	Subject = "Meet for lunch?",
	Body = body,
	ToRecipients = toRecipients,
	CcRecipients = ccRecipients,
};

var saveToSentItems = "false";

await graphClient.Me
	.sendMail(message,saveToSentItems);
	.Request()
	.PostAsync()

```