
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var tlpLevel = "green";

var threatType = "WatchList";

var targetProduct = "Azure Sentinel";

var tags = new List<String>();

var severity = 0;

var malwareFamilyNames = new List<String>();

var killChain = new List<String>();

var fileHashValue = "1796b433950990b28d6a22456c9d2b58ced1bdfcdf5f16f7e39d6b9bdca4213b";

var fileHashType = "sha256";

var externalId = "Test--8586509942423126760MS164-1";

var expirationDateTime = 3/2/2019 12:44:03 AM;

var description = "This is a canary indicator for demo purpose. Take no action on any observables set in this indicator.";

var confidence = 0;

var activityGroupNames = new List<String>();

var tlpLevel = "green";

var threatType = "WatchList";

var targetProduct = "Azure Sentinel";

var tags = new List<String>();

var severity = 0;

var malwareFamilyNames = new List<String>();

var killChain = new List<String>();

var fileHashValue = "b555c45c5b1b01304217e72118d6ca1b14b7013644a078273cea27bbdc1cf9d6";

var fileHashType = "sha256";

var externalId = "Test--8586509942423126760MS164-0";

var expirationDateTime = 3/2/2019 12:44:03 AM;

var description = "This is a canary indicator for demo purpose. Take no action on any observables set in this indicator.";

var confidence = 0;

var activityGroupNames = new List<String>();

var value = new List<TiIndicator>();
value.Add(new TiIndicator(activityGroupNames));
value.Add(new TiIndicator(confidence));
value.Add(new TiIndicator(description));
value.Add(new TiIndicator(expirationDateTime));
value.Add(new TiIndicator(externalId));
value.Add(new TiIndicator(fileHashType));
value.Add(new TiIndicator(fileHashValue));
value.Add(new TiIndicator(killChain));
value.Add(new TiIndicator(malwareFamilyNames));
value.Add(new TiIndicator(severity));
value.Add(new TiIndicator(tags));
value.Add(new TiIndicator(targetProduct));
value.Add(new TiIndicator(threatType));
value.Add(new TiIndicator(tlpLevel));
value.Add(new TiIndicator(activityGroupNames));
value.Add(new TiIndicator(confidence));
value.Add(new TiIndicator(description));
value.Add(new TiIndicator(expirationDateTime));
value.Add(new TiIndicator(externalId));
value.Add(new TiIndicator(fileHashType));
value.Add(new TiIndicator(fileHashValue));
value.Add(new TiIndicator(killChain));
value.Add(new TiIndicator(malwareFamilyNames));
value.Add(new TiIndicator(severity));
value.Add(new TiIndicator(tags));
value.Add(new TiIndicator(targetProduct));
value.Add(new TiIndicator(threatType));
value.Add(new TiIndicator(tlpLevel));

await graphClient.Security.TiIndicators
	.submitTiIndicators(value);
	.Request()
	.PostAsync()

```