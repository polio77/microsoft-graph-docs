
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var emailAddress = new EmailAddress
{
	Address = "danas@contoso.onmicrosoft.com",
	Name = "Dana Swope",
};

var ToRecipients = new List<String>();
ToRecipients.Add(new String(emailAddress));

var Comment = "Dana, hope you can make this meeting.";

await graphClient.Me.Events["{id}"]
	.forward(comment,toRecipients);
	.Request()
	.PostAsync()

```