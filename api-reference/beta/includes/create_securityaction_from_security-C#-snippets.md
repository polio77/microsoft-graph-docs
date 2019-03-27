
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var vendorInformation = new SecurityVendorInformation
{
	Provider = "Windows Defender ATP",
	Vendor = "Microsoft",
};

var value = "1.2.3.4";

var name = "IP";

var parameters = new List<KeyValuePair>();
parameters.Add(new KeyValuePair(name));
parameters.Add(new KeyValuePair(value));

var securityActions = new SecurityAction
{
	Name = "BlockIp",
	ActionReason = "Test",
	Parameters = parameters,
	VendorInformation = vendorInformation,
};

await graphClient.Security.SecurityActions
	.Request()
	.AddAsync(securityActions);

```