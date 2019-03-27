
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var body = new ItemBody
{
	ContentType = "",
	Content = "content-value",
};

var messages = new Message
{
	ReceivedDateTime = "datetime-value",
	SentDateTime = "datetime-value",
	HasAttachments = true,
	Subject = "subject-value",
	Body = body,
	BodyPreview = "bodyPreview-value",
};

await graphClient.Me.MailFolders["{id}"].Messages
	.Request()
	.AddAsync(messages);

```