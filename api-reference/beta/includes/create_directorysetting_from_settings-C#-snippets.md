
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = "value-value";

var name = "name-value";

var values = new List<SettingValue>();
values.Add(new SettingValue(name));
values.Add(new SettingValue(value));

var settings = new DirectorySetting
{
	TemplateId = "templateId-value",
	Values = values,
};

await graphClient.Settings
	.Request()
	.AddAsync(settings);

```