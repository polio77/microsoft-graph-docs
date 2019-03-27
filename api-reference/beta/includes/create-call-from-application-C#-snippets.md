
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var user = new Identity
{
	Id = "550fae72-d251-43ec-868c-373732c2704f",
	TenantId = "72f988bf-86f1-41af-91ab-2d7cd011db47",
	DisplayName = "Heidi Steen",
};

var identity = new IdentitySet
{
	User = user,
};

var targets = new List<ParticipantInfo>();
targets.Add(new ParticipantInfo(identity));

var application = new Identity
{
	Id = "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698",
};

var identity = new IdentitySet
{
	Application = application,
};

var source = new ParticipantInfo
{
	Identity = identity,
	LanguageId = "languageId-value",
	Region = "region-value",
};

var resourceId = "1D6DE2D4-CD51-4309-8DAA-70768651088F";

var uri = "https://cdn.contoso.com/cool.wav";

var resourceId = "1D6DE2D4-CD51-4309-8DAA-70768651088E";

var uri = "https://cdn.contoso.com/beep.wav";

var preFetchMedia = new List<>();
preFetchMedia.Add(new (uri));
preFetchMedia.Add(new (resourceId));
preFetchMedia.Add(new (uri));
preFetchMedia.Add(new (resourceId));

var mediaConfig = new MediaConfig
{
	@odata.type = "#microsoft.graph.serviceHostedMediaConfig",
	PreFetchMedia = preFetchMedia,
};

var calls = new Call
{
	CallbackUri = "https://bot.contoso.com/api/calls",
	MediaConfig = mediaConfig,
	Source = source,
	Subject = "Test Call",
	Targets = targets,
	TenantId = "tenantId-value",
};

await graphClient.App.Calls
	.Request()
	.AddAsync(calls);

```