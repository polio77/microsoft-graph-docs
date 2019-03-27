
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryObject = new 
{
};

var owners = new DirectoryObject
{
	DirectoryObject = directoryObject,
};

await graphClient.Applications["{id}"].Owners
	.Request()
	.AddAsync(owners);

```