
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var buckets = new PlannerBucket
{
	Name = "Advertising",
	PlanId = "xqQg5FS2LkCp935s-FIFm2QAFkHM",
	OrderHint = " !",
};

await graphClient.Planner.Buckets
	.Request()
	.AddAsync(buckets);

```