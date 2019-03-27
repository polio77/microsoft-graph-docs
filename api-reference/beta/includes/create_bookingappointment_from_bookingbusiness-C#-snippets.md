
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var start = new DateTimeTimeZone
{
	@odata.type = "#microsoft.graph.dateTimeTimeZone",
	DateTime = "2018-05-01T15:00:00+03:00",
	TimeZone = "UTC",
};

var address = new PhysicalAddress
{
	@odata.type = "#microsoft.graph.physicalAddress",
	City = "Buffalo",
	CountryOrRegion = "USA",
	PostalCode = "98052",
	PostOfficeBox = null,
	State = "NY",
	Street = "123 First Avenue",
	Type@odata.type = "#microsoft.graph.physicalAddressType",
	Type = null,
};

var serviceLocation = new Location
{
	@odata.type = "#microsoft.graph.location",
	Address = address,
	Coordinates = null,
	DisplayName = "Customer location",
	LocationEmailAddress = null,
	LocationType@odata.type = "#microsoft.graph.locationType",
	LocationType = null,
	LocationUri = null,
	UniqueId = null,
	UniqueIdType@odata.type = "#microsoft.graph.locationUniqueIdType",
	UniqueIdType = null,
};

var recipients = "staff";

var recipients@odata.type = "#microsoft.graph.bookingReminderRecipients";

var offset = "PT2H";

var message = "Please check traffic for next cater.";

var @odata.type = "#microsoft.graph.bookingReminder";

var recipients = "customer";

var recipients@odata.type = "#microsoft.graph.bookingReminderRecipients";

var offset = "PT1H";

var message = "Please be available to enjoy your lunch service.";

var @odata.type = "#microsoft.graph.bookingReminder";

var recipients = "allAttendees";

var recipients@odata.type = "#microsoft.graph.bookingReminderRecipients";

var offset = "P1D";

var message = "This service is tomorrow";

var @odata.type = "#microsoft.graph.bookingReminder";

var reminders = new List<BookingReminder>();
reminders.Add(new BookingReminder(@odata.type));
reminders.Add(new BookingReminder(message));
reminders.Add(new BookingReminder(offset));
reminders.Add(new BookingReminder(recipients@odata.type));
reminders.Add(new BookingReminder(recipients));
reminders.Add(new BookingReminder(@odata.type));
reminders.Add(new BookingReminder(message));
reminders.Add(new BookingReminder(offset));
reminders.Add(new BookingReminder(recipients@odata.type));
reminders.Add(new BookingReminder(recipients));
reminders.Add(new BookingReminder(@odata.type));
reminders.Add(new BookingReminder(message));
reminders.Add(new BookingReminder(offset));
reminders.Add(new BookingReminder(recipients@odata.type));
reminders.Add(new BookingReminder(recipients));

var invoiceDate = new DateTimeTimeZone
{
	@odata.type = "#microsoft.graph.dateTimeTimeZone",
	DateTime = "2018-05-01T15:30:00+03:00",
	TimeZone = "UTC",
};

var end = new DateTimeTimeZone
{
	@odata.type = "#microsoft.graph.dateTimeTimeZone",
	DateTime = "2018-05-01T15:30:00+03:00",
	TimeZone = "UTC",
};

var address = new PhysicalAddress
{
	@odata.type = "#microsoft.graph.physicalAddress",
	City = "Buffalo",
	CountryOrRegion = "USA",
	PostalCode = "98052",
	PostOfficeBox = null,
	State = "NY",
	Street = "123 First Avenue",
	Type@odata.type = "#microsoft.graph.physicalAddressType",
	Type = null,
};

var customerLocation = new Location
{
	@odata.type = "#microsoft.graph.location",
	Address = address,
	Coordinates = null,
	DisplayName = "Customer",
	LocationEmailAddress = null,
	LocationType@odata.type = "#microsoft.graph.locationType",
	LocationType = null,
	LocationUri = null,
	UniqueId = null,
	UniqueIdType@odata.type = "#microsoft.graph.locationUniqueIdType",
	UniqueIdType = null,
};

var appointments = new BookingAppointment
{
	@odata.type = "#microsoft.graph.bookingAppointment",
	CustomerEmailAddress = "jordanm@contoso.com",
	CustomerLocation = customerLocation,
	CustomerName = "Jordan Miller",
	CustomerNotes = "Please be on time.",
	CustomerPhone = "213-555-0199",
	End = end,
	InvoiceAmount = 10.0,
	InvoiceDate = invoiceDate,
	InvoiceId = "1001",
	InvoiceStatus@odata.type = "#microsoft.graph.bookingInvoiceStatus",
	InvoiceStatus = "open",
	InvoiceUrl = "theInvoiceUrl",
	OptOutOfCustomerEmail = false,
	PostBuffer = "PT10M",
	PreBuffer = "PT5M",
	Price = 10.0,
	PriceType@odata.type = "#microsoft.graph.bookingPriceType",
	PriceType = "fixedPrice",
	Reminders@odata.type = "#Collection(microsoft.graph.bookingReminder)",
	Reminders = reminders,
	ServiceId = "57da6774-a087-4d69-b0e6-6fb82c339976",
	ServiceLocation = serviceLocation,
	ServiceName = "Catered bento",
	ServiceNotes = "Customer requires punctual service.",
	Start = start,
};

await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].Appointments
	.Request()
	.AddAsync(appointments);

```