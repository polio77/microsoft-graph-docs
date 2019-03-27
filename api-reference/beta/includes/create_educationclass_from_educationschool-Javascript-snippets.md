
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

const classes = {
 @odata.id:"https://graph.microsoft.com/beta/education/classes/11006"
}
;

client.api('/education/schools/10002/classes/$ref')
	.version('beta').post({classes : classes});

```