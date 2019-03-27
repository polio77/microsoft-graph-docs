
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var item = new 
{
};

var attachments = new Attachment
{
	@odata.type = "#microsoft.graph.itemAttachment",
	Name = "name-value",
	Item = item,
};

await graphClient.Groups["{id}"].Threads["{id}"].Posts["{id}"].Attachments
	.Request()
	.AddAsync(attachments);

```