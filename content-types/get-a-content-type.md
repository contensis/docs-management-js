---
description: Gets an existing content type.
---
# Content types

## Get a content type

Gets an existing content type by the content type id or by passing a [ContentTypeGetOptions](/model/content-type-get-options.md) object as an argument.

 ***get(idOrOptions: string | ContentTypeGetOptions): Promise&lt;ContentType&gt;***

### Returns
A Promise that will resolve with a [ContentType](/model/content-type.md) object.

### Example
```js
client.contentTypes.get('movie')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});

client.contentTypes.get({
    id: 'movie',
    versionStatus: 'published'
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});

client.contentTypes.get({
    id: 'movie',
    version: '1.2'
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
