
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = "value-value";

var name = "name-value";

var values = new List<>();
values.Add(new (name));
values.Add(new (value));

var directorySetting = new 
{
	DisplayName = "displayName-value",
	TemplateId = "templateId-value",
	Values = values,
};

var settings = new DirectorySetting
{
	DirectorySetting = directorySetting,
};

await graphClient.Groups["{id}"].Settings
	.Request()
	.AddAsync(settings);

```