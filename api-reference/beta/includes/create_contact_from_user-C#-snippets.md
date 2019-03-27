
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var type = "business";

var number = "+1 732 555 0102";

var phones = new List<Phone>();
phones.Add(new Phone(number));
phones.Add(new Phone(type));

var otherLabel = "Volunteer work";

var type = "other";

var name = "Pavel Bansky";

var address = "pavelb@fabrikam.onmicrosoft.com";

var type = "personal";

var name = "Pavel Bansky";

var address = "pavelb@contoso.onmicrosoft.com";

var emailAddresses = new List<TypedEmailAddress>();
emailAddresses.Add(new TypedEmailAddress(address));
emailAddresses.Add(new TypedEmailAddress(name));
emailAddresses.Add(new TypedEmailAddress(type));
emailAddresses.Add(new TypedEmailAddress(address));
emailAddresses.Add(new TypedEmailAddress(name));
emailAddresses.Add(new TypedEmailAddress(type));
emailAddresses.Add(new TypedEmailAddress(otherLabel));

var contacts = new Contact
{
	GivenName = "Pavel",
	Surname = "Bansky",
	EmailAddresses = emailAddresses,
	Phones = phones,
};

await graphClient.Me.Contacts
	.Request()
	.AddAsync(contacts);

```