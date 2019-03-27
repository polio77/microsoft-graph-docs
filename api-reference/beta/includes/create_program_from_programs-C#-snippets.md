
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var programs = new Program
{
	DisplayName = "testprogram3",
	Description = "test description",
};

await graphClient.Programs
	.Request()
	.AddAsync(programs);

```