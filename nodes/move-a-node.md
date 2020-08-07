---
description: Moves a node.
---
# Move a node

Moves a node.

This is a special case of [updating a node.](update-a-node.md) By changing the parent id of a node and updating the node and all of its children will be moved so that they are now descendants of the parent node, with the same hierarchical structure.

***update(node: Node): Promise&lt;Node&gt;***

### Example

```js
let node = {
    "id": "d6bdea41-729c-4a07-85bf-a392aa0afc2b",
	 // Change the parent id to move the node
    "parentId": "f3322e4f-72b5-4064-be88-fcfed6c82635",
    "displayName": {
        "en-GB": "Tiger Escaped From Zoo"
    },
    "slug": {
        "en-GB": "tiger-escaped-from-zoo"
    },
    "entryId": "9272ac06-1b3a-4e68-ac1b-a05828b0f7d6"
};
client.nodes.update(node)
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
