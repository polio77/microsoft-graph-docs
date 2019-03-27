
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryObject = new 
{
};

var memberOf = new DirectoryObject
{
	DirectoryObject = directoryObject,
};

await graphClient.Contacts["{id}"].MemberOf
	.Request()
	.AddAsync(memberOf);

```