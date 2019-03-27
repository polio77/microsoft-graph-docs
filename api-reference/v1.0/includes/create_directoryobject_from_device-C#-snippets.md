
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryObject = new 
{
};

var registeredUsers = new DirectoryObject
{
	DirectoryObject = directoryObject,
};

await graphClient.Devices["{id}"].RegisteredUsers
	.Request()
	.AddAsync(registeredUsers);

```