
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var attachments = new Attachment
{
	@odata.type = "#microsoft.graph.fileAttachment",
	Name = "smile",
	ContentBytes = "R0lGODdhEAYEAA7",
};

await graphClient.Me.Messages["AAMkpsDRVK"].Attachments
	.Request()
	.AddAsync(attachments);

```