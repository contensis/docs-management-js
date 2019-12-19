---
description: Creates a new content type resource.
---

# Update a content type

Updates a content type resource.

***update(contentType: ContentType): Promise&lt;ContentType&gt;***

## Returns

A Promise that will resolve with a [ContentType](/model/content-type.md) object.

## Example

```js
existingContentType.description['en-GB'] = 'A movie content type';

client.contentTypes.update(existingContentType)
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
  });
```
