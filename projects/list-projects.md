---
description: Returns a list of the project resources for a Contensis instance.
---
## List projects

Returns a list of the project resources for a Contensis instance.


***list(): Promise&lt;Project&gt;[]***

### Returns
A Promise that will resolve with an array of [Project](/model/project.md) objects.

### Example

```js
client.projects.list()
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
