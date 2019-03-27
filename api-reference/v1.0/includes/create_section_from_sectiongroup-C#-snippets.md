
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var sections = new OnenoteSection
{
	DisplayName = "Section name",
};

await graphClient.Me.Onenote.SectionGroups["{id}"].Sections
	.Request()
	.AddAsync(sections);

```