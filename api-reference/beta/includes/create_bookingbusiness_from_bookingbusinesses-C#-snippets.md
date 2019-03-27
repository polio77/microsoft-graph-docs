
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var address = new PhysicalAddress
{
	Type = "mall",
	PostOfficeBox = "P.O. Box 123",
	Street = "4567 Main Street",
	City = "Buffalo",
	State = "NY",
	CountryOrRegion = "USA",
	PostalCode = "98052",
};

var bookingBusinesses = new BookingBusiness
{
	DisplayName = "Fourth Coffee",
	Address = address,
	Phone = "206-555-0100",
	Email = "manager@fourthcoffee.com",
	WebSiteUrl = "https://www.fourthcoffee.com",
	DefaultCurrencyIso = "USD",
};

await graphClient.BookingBusinesses
	.Request()
	.AddAsync(bookingBusinesses);

```