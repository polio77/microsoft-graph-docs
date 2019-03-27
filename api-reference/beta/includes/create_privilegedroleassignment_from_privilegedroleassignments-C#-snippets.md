
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var privilegedRoleAssignments = new PrivilegedRoleAssignment
{
	UserId = "userId-value",
	RoleId = "roleId-value",
};

await graphClient.PrivilegedRoleAssignments
	.Request()
	.AddAsync(privilegedRoleAssignments);

```