
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var emailAddress = new EmailAddress
{
	Name = "Adele Vance",
	Address = "AdeleV@contoso.onmicrosoft.com",
};

var newParticipants = new List<Recipient>();
newParticipants.Add(new Recipient(emailAddress));

var body = new ItemBody
{
	ContentType = "html",
	Content = "The confirmation will come by the end of the week.",
};

var posts = new List<Post>();
posts.Add(new Post(body));
posts.Add(new Post(newParticipants));

var threads = new List<ConversationThread>();
threads.Add(new ConversationThread(posts));

var conversations = new Conversation
{
	Topic = "New head count",
	Threads = threads,
};

await graphClient.Groups["29981b6a-0e57-42dc-94c9-cd24f5306196"].Conversations
	.Request()
	.AddAsync(conversations);

```