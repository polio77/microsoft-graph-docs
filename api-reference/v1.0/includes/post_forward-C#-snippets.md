
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var comment = "comment-value";

var emailAddress = new EmailAddress
{
	Name = "name-value",
	Address = "address-value",
};

var toRecipients = new List<String>();
toRecipients.Add(new String(emailAddress));

await graphClient.Groups["{id}"].Threads["{id}"].Posts["{id}"]
	.forward(comment,toRecipients);
	.Request()
	.PostAsync()

```