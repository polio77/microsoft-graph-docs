
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var businessPhones = new List<String>();

var name = "Pavel Bansky";

var address = "pavelb@fabrikam.onmicrosoft.com";

var emailAddresses = new List<EmailAddress>();
emailAddresses.Add(new EmailAddress(address));
emailAddresses.Add(new EmailAddress(name));

var contacts = new Contact
{
	GivenName = "Pavel",
	Surname = "Bansky",
	EmailAddresses = emailAddresses,
	BusinessPhones = businessPhones,
};

await graphClient.Me.Contacts
	.Request()
	.AddAsync(contacts);

```