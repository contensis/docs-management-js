---
description: API instantiation describes how to configure and use the client API.
---

# API instantiation

## Installing and importing the client *npm* package

The Contensis JS Management API client is delivered as an [*npm*](https://www.npmjs.com/package/contensis-management-api) package, with publicly available [source code](https://github.com/contensis/contensis-management-api) and [examples](https://github.com/contensis/contensis-management-api-examples).  
The client package mainly targets Node.js as a runtime platform and should be used in a server side context (e.g. a Node.js console application, an Express.js web application).

> ### Note
> Before following the rest of the examples we assume you have an existing Node.js or Express.js application that is already created, that targets Node.js >= 10 and uses the *CommonJS* module system (you can also use native JavaScript modules - see [examples](https://github.com/contensis/contensis-management-api-examples)).  
> The Contensis JS Management API client is using the *fetch* API to maintain consistency with the Contensis JS Delivery API client. The *fetch* API is not a native Node.js API and it is loaded automatically from the *node-fetch* npm package when the Contensis JS Management API client runs in a Node.js environment (if it runs in a browser enviroment the native *fetch* API will be used instead).  

To install the required packages for the Contensis JS Management API client please run the following Node.js command line:
```
npm install contensis-management-api
```
To import this package your JavaScript code file should have the following line at the top:
```js
const Client = require('contensis-management-api').Client;
```
## Creating and using the client instance 

All operations for the API hang off the `Client` type, which is created using the static method call `Client.create(options)`. The `options` object represents the shared configuration that will be used by all Management API calls and is of type [Config](/model/config.md):

```js
const client = Client.create({
  clientType: "client_credentials",
  clientDetails: {
    clientId: '6f8cf1e8-b2ee-49ad-9b94-2dbb09871903',
    clientSecret: '6d80c9a356ce4317bd71d92c5734d67a-4a837b1336344f63b1b24ce2dfa73945-ef09daa8d0f74b1e8e223779c392a67b'
  }
  projectId: 'website',
  rootUrl: 'https://cms-example.cloud.contensis.com'
});

client.contentTypes.list()
  .then(result => {      
      console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
  });
```
