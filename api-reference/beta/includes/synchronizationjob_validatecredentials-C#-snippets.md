
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = "password-value";

var key = "Password";

var value = "user@domain.com";

var key = "UserName";

var credentials = new List<String>();
credentials.Add(new String(key));
credentials.Add(new String(value));
credentials.Add(new String(key));
credentials.Add(new String(value));

await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs["{id}"]
	.validateCredentials(applicationIdentifier,templateId,useSavedCredentials,credentials);
	.Request()
	.PostAsync()

```