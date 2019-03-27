
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var skuId = "skuId-value-2";

var disabledPlans = new List<Guid>();

var skuId = "skuId-value-1";

var disabledPlans = new List<Guid>();

var addLicenses = new List<AssignedLicense>();
addLicenses.Add(new AssignedLicense(disabledPlans));
addLicenses.Add(new AssignedLicense(skuId));
addLicenses.Add(new AssignedLicense(disabledPlans));
addLicenses.Add(new AssignedLicense(skuId));

var removeLicenses = new List<AssignedLicense>();

await graphClient.Me
	.assignLicense(addLicenses,removeLicenses);
	.Request()
	.PostAsync()

```