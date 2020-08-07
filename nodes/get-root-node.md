---
description: Get root node.
---
# Get the root node

Get the root node of the current project.

 ***getRoot(): Promise&lt;Node&gt;***

### Returns
A Promise that will resolve with a [Node](/model/node.md) object.

### Example

```js
client.nodes.getRoot()
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
