
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var attachments = new Attachment
{
	@odata.type = "#microsoft.graph.fileAttachment",
	Name = "menu.txt",
	ContentBytes = "bWFjIGFuZCBjaGVlc2UgdG9kYXk=",
};

await graphClient.Me.Events["AAMkAGI1AAAt9AHjAAA="].Attachments
	.Request()
	.AddAsync(attachments);

```