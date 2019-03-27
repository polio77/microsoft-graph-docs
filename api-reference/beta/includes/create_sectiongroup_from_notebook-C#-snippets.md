
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var sectionGroups = new SectionGroup
{
	DisplayName = "Section group name",
};

await graphClient.Me.Onenote.Notebooks["{id}"].SectionGroups
	.Request()
	.AddAsync(sectionGroups);

```