
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var topPicks = new List<>();

var expirationDate = 8/3/2016 11:00:00 AM;

var companyName = "Contoso";

var extensionName = "Com.Contoso.Benefits";

var @odata.type = "Microsoft.OutlookServices.OpenTypeExtension";

var Extensions = new List<>();
Extensions.Add(new (@odata.type));
Extensions.Add(new (extensionName));
Extensions.Add(new (companyName));
Extensions.Add(new (expirationDate));
Extensions.Add(new (topPicks));

var Body = new 
{
	ContentType = "HTML",
	Content = "This is urgent!",
};

var Posts = new List<>();
Posts.Add(new (Body));
Posts.Add(new (Extensions));

var Threads = new List<>();
Threads.Add(new (Posts));

var conversations = new Conversation
{
	Topic = "Does anyone have a second?",
	Threads = Threads,
};

await graphClient.Groups["37df2ff0-0de0-4c33-8aee-75289364aef6"].Conversations
	.Request()
	.AddAsync(conversations);

```