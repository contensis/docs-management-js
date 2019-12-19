---
description: Gets the content types for a project.
---
# List content types

Gets the content types for a project by passing an optional [ContentTypeListOptions](/model/content-type-list-options.md) object as an argument.

***list(options?: ContentTypeListOptions): Promise&lt;ContentType[]&gt;***

## Returns

A Promise that will resolve with an array of [ContentType](/model/content-type.md) objects.

## Example

```js
client.contentTypes.list({    
    versionStatus: 'published',
    dataFormat: 'entry'
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
