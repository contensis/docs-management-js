---
description: Deletes a content type within a specific project.
---

# Delete a content type

Deletes a content type from a specific project.

***delete(id: string): Promise&lt;void&gt;***

## Returns
A Promise that will resolve with an empty object.

## Example

```js
client.contentTypes.delete('movie')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
