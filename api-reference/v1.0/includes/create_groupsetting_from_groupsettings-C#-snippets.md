
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = "value-value";

var name = "name-value";

var values = new List<SettingValue>();
values.Add(new SettingValue(name));
values.Add(new SettingValue(value));

var groupSettings = new GroupSetting
{
	DisplayName = "displayName-value",
	TemplateId = "templateId-value",
	Values = values,
};

await graphClient.GroupSettings
	.Request()
	.AddAsync(groupSettings);

```