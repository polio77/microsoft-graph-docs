
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var administrativeUnits = new AdministrativeUnit
{
	DisplayName = "Seattle District Technical Schools",
	Description = "Seattle district technical schools administration",
	Visibility = "true",
};

await graphClient.AdministrativeUnits
	.Request()
	.AddAsync(administrativeUnits);

```