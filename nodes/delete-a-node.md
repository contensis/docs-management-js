---
description: Deletes a node.
---
# Delete a node

Deletes a node by id.

***delete(id: string): Promise&lt;void&gt;***

### Example

```js
client.nodes.delete('c31111e7-76f7-46dd-93fb-cbf81a853a37')
  .then(result => {      
    console.log('API call was successful');              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```