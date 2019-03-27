
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var inputIds = new List<String>();

var sourceIdType = "restId";

var targetIdType = "restImmutableEntryId";

await graphClient.Me
	.translateExchangeIds(inputIds,targetIdType,sourceIdType);
	.Request()
	.PostAsync()

```