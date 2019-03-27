
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var body = new ItemBody
{
	ContentType = "",
	Content = "content-value",
};

var post = new Post
{
	Body = body,
};

await graphClient.Groups["{id}"].Threads["{id}"]
	.reply(post);
	.Request()
	.PostAsync()

```