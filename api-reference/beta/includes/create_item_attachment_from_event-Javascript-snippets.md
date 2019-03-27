
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
  name: "Holiday event",
  item: {
        @odata.type: "microsoft.graph.event",
        subject: "Discuss gifts for children",
        body: {
            contentType: "HTML",
            content: "Let's look for funding!"
         },
         start: {
             dateTime: "2016-12-02T18:00:00",
             timeZone: "Pacific Standard Time"
          },
          end: {
             dateTime: "2016-12-02T19:00:00",
             timeZone: "Pacific Standard Time"
          }
    }
}
;

client.api('/me/events/{AAMkAGI1AAAt9AHjAAA=}/attachments')
	.version('beta').post({attachments : attachments});

```