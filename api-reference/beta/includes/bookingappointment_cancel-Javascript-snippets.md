
```Javascript

// Some callback function
const authProvider: AuthProvider = (callback: AuthProviderCallback) => { 
	// Your logic for getting and refreshing accessToken 
	// Error should be passed in case of error while authenticating 
	// accessToken should be passed upon successful authentication 
	callback(error, accessToken);
};

let options: Options = {
		authProvider,
};

const client = Client.init(options);

const cancel = {
  cancellationMessage: "Your appointment has been successfully cancelled. Please call us again."
}
;

client.api('/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/appointments/AAMkADKoAAA=/cancel')
	.version('beta').post({cancel : cancel});

```