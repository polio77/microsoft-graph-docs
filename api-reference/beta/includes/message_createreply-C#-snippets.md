
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var emailAddress = new EmailAddress
{
	Address = "randiw@contoso.onmicrosoft.com",
	Name = "Randi Welch",
};

var emailAddress = new EmailAddress
{
	Address = "samanthab@contoso.onmicrosoft.com",
	Name = "Samantha Booth",
};

var toRecipients = new List<Recipient>();
toRecipients.Add(new Recipient(emailAddress));
toRecipients.Add(new Recipient(emailAddress));

var message = new Message
{
	ToRecipients = toRecipients,
};

var comment = "Samantha, Randi, would you name the group if the project is approved, please?";

await graphClient.Me.Messages["AAMkADA1MTAAAAqldOAAA="]
	.createReply(message,comment);
	.Request()
	.PostAsync()

```