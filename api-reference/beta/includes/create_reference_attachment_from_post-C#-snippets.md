
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var attachments = new Attachment
{
	@odata.type = "#microsoft.graph.referenceAttachment",
	Name = "Personal pictures",
	SourceUrl = "https://contoso.com/personal/mario_contoso_net/Documents/Pics",
	ProviderType = "oneDriveConsumer",
	Permission = "Edit",
	IsFolder = "True",
};

await graphClient.Groups["c75831bdfad"].Threads["AAQkAGF97XEKhULw"].Posts["AAMkAGFcAAA"].Attachments
	.Request()
	.AddAsync(attachments);

```