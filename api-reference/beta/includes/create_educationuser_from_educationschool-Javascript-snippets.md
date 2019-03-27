
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

const users = {
  @odata.id:"https://graph.microsoft.com/beta/education/users/14008"
}
;

client.api('/education/schools/<id>/users/$ref')
	.version('beta').post({users : users});

```