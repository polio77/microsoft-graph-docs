
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var emailAddress = new EmailAddress
{
	Address = "danas@contoso.onmicrosoft.com",
	Name = "Dana Swope",
};

var toRecipients = new List<Recipient>();
toRecipients.Add(new Recipient(emailAddress));

var message = new Message
{
	IsDeliveryReceiptRequested = true,
	ToRecipients = toRecipients,
};

var comment = "Dana, just want to make sure you get this.";

await graphClient.Me.Messages["AAMkADA1MTAAAH5JaLAAA="]
	.forward(message,comment,toRecipients);
	.Request()
	.PostAsync()

```