
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

const members = {
  @odata.id: "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
}
;

client.api('/directoryRoles/{id}/members/$ref').post({members : members});

```