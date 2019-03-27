
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

const attachments = {
  @odata.type: "#microsoft.graph.itemAttachment",
  name: "name-value",
  item: { }
}
;

client.api('/groups/{id}/threads/{id}/posts/{id}/attachments')
	.version('beta').post({attachments : attachments});

```