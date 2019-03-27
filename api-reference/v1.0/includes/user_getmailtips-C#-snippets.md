
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var EmailAddresses = new List<String>();

var MailTipsOptions = "automaticReplies, mailboxFullStatus";

await graphClient.Me
	.getMailTips(emailAddresses,mailTipsOptions);
	.Request()
	.PostAsync()

```