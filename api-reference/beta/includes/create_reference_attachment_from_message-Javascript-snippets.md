
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
    @odata.type: "#microsoft.graph.referenceAttachment", 
    name: "Personal pictures", 
    sourceUrl: "https://contoso.com/personal/mario_contoso_net/Documents/Pics", 
    providerType: "oneDriveConsumer", 
    permission: "Edit", 
    isFolder: "True" 
} 
;

client.api('/me/messages/AAMkAGE1M88AADUv0uFAAA=/attachments')
	.version('beta').post({attachments : attachments});

```