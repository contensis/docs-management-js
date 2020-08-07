---
description: Get a node.
---
# Get a node

Get a node by id.

***get(id: string): Promise&lt;Node&gt;***

### Returns
A Promise that will resolve with a [Node](/model/node.md) object.

### Example

```js
client.nodes.get('c31111e7-76f7-46dd-93fb-cbf81a853a37')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
