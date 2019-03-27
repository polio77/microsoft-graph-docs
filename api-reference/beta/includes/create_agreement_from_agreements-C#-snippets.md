
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var fileData = new AgreementFileData
{
	Data = "SGVsbG8gd29ybGQ=",
};

var isDefault = True;

var language = "en";

var fileName = "TOU.pdf";

var files = new List<AgreementFile>();
files.Add(new AgreementFile(fileName));
files.Add(new AgreementFile(language));
files.Add(new AgreementFile(isDefault));
files.Add(new AgreementFile(fileData));

var agreements = new Agreement
{
	DisplayName = "MSGraph Sample",
	IsViewingBeforeAcceptanceRequired = true,
	Files = files,
};

await graphClient.Agreements
	.Request()
	.AddAsync(agreements);

```