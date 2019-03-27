
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var passwordProfile = new PasswordProfile
{
	ForceChangePasswordNextSignIn = true,
	Password = "password-value",
};

var users = new User
{
	AccountEnabled = true,
	DisplayName = "displayName-value",
	MailNickname = "mailNickname-value",
	UserPrincipalName = "upn-value@tenant-value.onmicrosoft.com",
	PasswordProfile = passwordProfile,
};

await graphClient.Users
	.Request()
	.AddAsync(users);

```