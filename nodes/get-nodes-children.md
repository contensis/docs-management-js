---
description: Gets the node's children.
---
# Get node's children

Get all the children of a specific node by specifying the node id or a [NodeGetChildrenOptions](/model/node-get-children-options.md) object.

***getChildren(idOrOptions: string | NodeGetChildrenOptions): Promise&lt;Node[]&gt;***

### Example

```js
client.nodes.getChildren('c31111e7-76f7-46dd-93fb-cbf81a853a37')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});

client.nodes.getChildren({ id: 'c31111e7-76f7-46dd-93fb-cbf81a853a37',  language: 'fr-FR' })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
