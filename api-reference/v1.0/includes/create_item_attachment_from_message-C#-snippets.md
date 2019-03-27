
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var end = new 
{
	DateTime = "2016-12-02T19:00:00",
	TimeZone = "Pacific Standard Time",
};

var start = new 
{
	DateTime = "2016-12-02T18:00:00",
	TimeZone = "Pacific Standard Time",
};

var body = new 
{
	ContentType = "HTML",
	Content = "Let's look for funding!",
};

var item = new 
{
	@odata.type = "microsoft.graph.event",
	Subject = "Discuss gifts for children",
	Body = body,
	Start = start,
	End = end,
};

var attachments = new Attachment
{
	@odata.type = "#microsoft.graph.itemAttachment",
	Name = "Holiday event",
	Item = item,
};

await graphClient.Me.Messages["AAMkpsDRVK"].Attachments
	.Request()
	.AddAsync(attachments);

```