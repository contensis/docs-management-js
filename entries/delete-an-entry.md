---
description: Deletes an entry by its Id.
---
# Delete an entry

Deletes an entry or specific variations by id.

***delete(id: string, languages?: string[]): Promise&lt;void&gt;***

## Returns
A Promise that will resolve with an empty object.

## Example

```js
client.entries.delete('fa9bf8d8-c7f2-4fed-ae38-e7b1b2935d1c')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});

client.entries.delete('fa9bf8d8-c7f2-4fed-ae38-e7b1b2935d1c', ['fr', 'fr-FR'])
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
