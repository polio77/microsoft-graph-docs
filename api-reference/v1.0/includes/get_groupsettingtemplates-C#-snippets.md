
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupSettingTemplates = await graphClient.GroupSettingTemplates
	.Request()
	.GetAsync();

```