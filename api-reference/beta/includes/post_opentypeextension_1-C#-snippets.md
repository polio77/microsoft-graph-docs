
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var dealValue = 10000;

var expirationDate = 12/30/2015 11:00:00 AM;

var companyName = "Wingtip Toys";

var extensionName = "Com.Contoso.Referral";

var @odata.type = "Microsoft.Graph.OpenTypeExtension";

var extensions = new List<Extension>();
extensions.Add(new Extension(@odata.type));
extensions.Add(new Extension(extensionName));
extensions.Add(new Extension(companyName));
extensions.Add(new Extension(expirationDate));
extensions.Add(new Extension(dealValue));

var emailAddress = new EmailAddress
{
	Address = "rufus@contoso.com",
};

var toRecipients = new List<Recipient>();
toRecipients.Add(new Recipient(emailAddress));

var body = new ItemBody
{
	ContentType = "HTML",
	Content = "You should be proud!",
};

var messages = new Message
{
	Subject = "Annual review",
	Body = body,
	ToRecipients = toRecipients,
	Extensions = extensions,
};

await graphClient.Me.Messages
	.Request()
	.AddAsync(messages);

```