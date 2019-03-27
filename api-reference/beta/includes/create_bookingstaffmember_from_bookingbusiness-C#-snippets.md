
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var start = "08:00:00.0000000";

var end = "17:00:00.0000000";

var @odata.type = "#microsoft.graph.bookingWorkTimeSlot";

var timeSlots = new List<BookingWorkTimeSlot>();
timeSlots.Add(new BookingWorkTimeSlot(@odata.type));
timeSlots.Add(new BookingWorkTimeSlot(end));
timeSlots.Add(new BookingWorkTimeSlot(start));

var timeSlots@odata.type = "#Collection(microsoft.graph.bookingWorkTimeSlot)";

var day = "friday";

var day@odata.type = "#microsoft.graph.dayOfWeek";

var @odata.type = "#microsoft.graph.bookingWorkHours";

var start = "08:00:00.0000000";

var end = "17:00:00.0000000";

var @odata.type = "#microsoft.graph.bookingWorkTimeSlot";

var timeSlots = new List<BookingWorkTimeSlot>();
timeSlots.Add(new BookingWorkTimeSlot(@odata.type));
timeSlots.Add(new BookingWorkTimeSlot(end));
timeSlots.Add(new BookingWorkTimeSlot(start));

var timeSlots@odata.type = "#Collection(microsoft.graph.bookingWorkTimeSlot)";

var day = "thursday";

var day@odata.type = "#microsoft.graph.dayOfWeek";

var @odata.type = "#microsoft.graph.bookingWorkHours";

var start = "08:00:00.0000000";

var end = "17:00:00.0000000";

var @odata.type = "#microsoft.graph.bookingWorkTimeSlot";

var timeSlots = new List<BookingWorkTimeSlot>();
timeSlots.Add(new BookingWorkTimeSlot(@odata.type));
timeSlots.Add(new BookingWorkTimeSlot(end));
timeSlots.Add(new BookingWorkTimeSlot(start));

var timeSlots@odata.type = "#Collection(microsoft.graph.bookingWorkTimeSlot)";

var day = "wednesday";

var day@odata.type = "#microsoft.graph.dayOfWeek";

var @odata.type = "#microsoft.graph.bookingWorkHours";

var start = "08:00:00.0000000";

var end = "17:00:00.0000000";

var @odata.type = "#microsoft.graph.bookingWorkTimeSlot";

var timeSlots = new List<BookingWorkTimeSlot>();
timeSlots.Add(new BookingWorkTimeSlot(@odata.type));
timeSlots.Add(new BookingWorkTimeSlot(end));
timeSlots.Add(new BookingWorkTimeSlot(start));

var timeSlots@odata.type = "#Collection(microsoft.graph.bookingWorkTimeSlot)";

var day = "tuesday";

var day@odata.type = "#microsoft.graph.dayOfWeek";

var @odata.type = "#microsoft.graph.bookingWorkHours";

var start = "08:00:00.0000000";

var end = "17:00:00.0000000";

var @odata.type = "#microsoft.graph.bookingWorkTimeSlot";

var timeSlots = new List<BookingWorkTimeSlot>();
timeSlots.Add(new BookingWorkTimeSlot(@odata.type));
timeSlots.Add(new BookingWorkTimeSlot(end));
timeSlots.Add(new BookingWorkTimeSlot(start));

var timeSlots@odata.type = "#Collection(microsoft.graph.bookingWorkTimeSlot)";

var day = "monday";

var day@odata.type = "#microsoft.graph.dayOfWeek";

var @odata.type = "#microsoft.graph.bookingWorkHours";

var workingHours = new List<BookingWorkHours>();
workingHours.Add(new BookingWorkHours(@odata.type));
workingHours.Add(new BookingWorkHours(day@odata.type));
workingHours.Add(new BookingWorkHours(day));
workingHours.Add(new BookingWorkHours(timeSlots@odata.type));
workingHours.Add(new BookingWorkHours(timeSlots));
workingHours.Add(new BookingWorkHours(@odata.type));
workingHours.Add(new BookingWorkHours(day@odata.type));
workingHours.Add(new BookingWorkHours(day));
workingHours.Add(new BookingWorkHours(timeSlots@odata.type));
workingHours.Add(new BookingWorkHours(timeSlots));
workingHours.Add(new BookingWorkHours(@odata.type));
workingHours.Add(new BookingWorkHours(day@odata.type));
workingHours.Add(new BookingWorkHours(day));
workingHours.Add(new BookingWorkHours(timeSlots@odata.type));
workingHours.Add(new BookingWorkHours(timeSlots));
workingHours.Add(new BookingWorkHours(@odata.type));
workingHours.Add(new BookingWorkHours(day@odata.type));
workingHours.Add(new BookingWorkHours(day));
workingHours.Add(new BookingWorkHours(timeSlots@odata.type));
workingHours.Add(new BookingWorkHours(timeSlots));
workingHours.Add(new BookingWorkHours(@odata.type));
workingHours.Add(new BookingWorkHours(day@odata.type));
workingHours.Add(new BookingWorkHours(day));
workingHours.Add(new BookingWorkHours(timeSlots@odata.type));
workingHours.Add(new BookingWorkHours(timeSlots));

var staffMembers = new BookingStaffMember
{
	@odata.type = "#microsoft.graph.bookingStaffMember",
	ColorIndex = 1,
	DisplayName = "Dana Swope",
	EmailAddress = "danas@contoso.com",
	Role@odata.type = "#microsoft.graph.bookingStaffRole",
	Role = "externalGuest",
	UseBusinessHours = true,
	WorkingHours@odata.type = "#Collection(microsoft.graph.bookingWorkHours)",
	WorkingHours = workingHours,
};

await graphClient.BookingBusinesses["{id}"].StaffMembers
	.Request()
	.AddAsync(staffMembers);

```