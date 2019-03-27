
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var attachments = new Attachment
{
	@odata.type = "#Microsoft.OutlookServices.ItemAttachment",
	Name = "name-value",
	Item = "message or event entity",
};

await graphClient.Me.Events["{id}"].Attachments
	.Request()
	.AddAsync(attachments);

```