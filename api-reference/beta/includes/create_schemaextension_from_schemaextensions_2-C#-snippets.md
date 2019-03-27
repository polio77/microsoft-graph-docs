
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var type = "String";

var name = "courseType";

var type = "String";

var name = "courseName";

var type = "Integer";

var name = "courseId";

var properties = new List<ExtensionSchemaProperty>();
properties.Add(new ExtensionSchemaProperty(name));
properties.Add(new ExtensionSchemaProperty(type));
properties.Add(new ExtensionSchemaProperty(name));
properties.Add(new ExtensionSchemaProperty(type));
properties.Add(new ExtensionSchemaProperty(name));
properties.Add(new ExtensionSchemaProperty(type));

var targetTypes = new List<String>();

var schemaExtensions = new SchemaExtension
{
	Id = "courses",
	Description = "Graph Learn training courses extensions",
	TargetTypes = targetTypes,
	Properties = properties,
};

await graphClient.SchemaExtensions
	.Request()
	.AddAsync(schemaExtensions);

```