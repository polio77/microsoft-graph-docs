
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var extensions = new Extension
{
	@odata.type = "Microsoft.Graph.OpenTypeExtension",
	ExtensionName = "Com.Contoso.Deal",
	CompanyName = "Alpine Skis",
	DealValue = 1010100,
	ExpirationDate = "2015-07-03T13:04:00Z",
};

await graphClient.Groups["f5480dfd-7d77-4d0b-ba2e-3391953cc74a"].Events["AAMkADVl17IsAAA="].Extensions
	.Request()
	.AddAsync(extensions);

```