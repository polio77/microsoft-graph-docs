
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var emailAddress = new EmailAddress
{
	Name = "Alex Wilbur",
	Address = "AlexW@contoso.onmicrosoft.com",
};

var forwardTo = new List<Recipient>();
forwardTo.Add(new Recipient(emailAddress));

var actions = new MessageRuleActions
{
	ForwardTo = forwardTo,
	StopProcessingRules = true,
};

var senderContains = new List<String>();

var conditions = new MessageRulePredicates
{
	SenderContains = senderContains,
};

var messageRules = new MessageRule
{
	DisplayName = "From partner",
	Sequence = 2,
	IsEnabled = true,
	Conditions = conditions,
	Actions = actions,
};

await graphClient.Me.MailFolders["inbox"].MessageRules
	.Request()
	.AddAsync(messageRules);

```