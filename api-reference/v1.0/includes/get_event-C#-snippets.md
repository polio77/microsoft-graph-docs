
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var events = await graphClient.Me.Events["AAMkAGIAAAoZDOFAAA="]
	.Request()
	.Header("Prefer","outlook.timezone="Pacific Standard Time"")
	.Select("subject,body,bodyPreview,organizer,attendees,start,end,location")
	.GetAsync();

```