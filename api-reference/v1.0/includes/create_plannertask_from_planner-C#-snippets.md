
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var fbab97d0-4932-4511-b675-204639209557 = new 
{
	@odata.type = "#microsoft.graph.plannerAssignment",
	OrderHint = " !",
};

var assignments = new PlannerAssignments
{
	Fbab97d0-4932-4511-b675-204639209557 = fbab97d0-4932-4511-b675-204639209557,
};

var tasks = new PlannerTask
{
	PlanId = "xqQg5FS2LkCp935s-FIFm2QAFkHM",
	BucketId = "hsOf2dhOJkqyYYZEtdzDe2QAIUCR",
	Title = "Update client list",
	Assignments = assignments,
};

await graphClient.Planner.Tasks
	.Request()
	.AddAsync(tasks);

```