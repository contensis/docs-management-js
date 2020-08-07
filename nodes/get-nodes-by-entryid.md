---
description: Get nodes that have a specified entry attached.
---
# Get nodes by entry id

Get all nodes that have a specified entry attached.

***getByEntryId(entryId: string): Promise&lt;Node[]&gt;***

### Example

```js
client.nodes.getByEntryId('273b8bfa-5dfe-409b-872d-95e6a72f6bc9')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```