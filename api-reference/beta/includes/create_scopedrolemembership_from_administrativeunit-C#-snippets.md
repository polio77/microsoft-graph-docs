
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var roleMemberInfo = new Identity
{
	Id = "id-value",
};

var scopedRoleMembers = new ScopedRoleMembership
{
	RoleId = "roleId-value",
	RoleMemberInfo = roleMemberInfo,
};

await graphClient.AdministrativeUnits["{id}"].ScopedRoleMembers
	.Request()
	.AddAsync(scopedRoleMembers);

```