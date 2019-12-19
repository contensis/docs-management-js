---
description: Projects offer a way of grouping related content types, entries and assets.
---
# Projects

Projects offer a way of grouping related content types, entries and assets. Typically a project would represent a single application such as a website, intranet or mobile application.

Projects are a licensed feature and the number you can create will depend on which license you have purchased.


## Get a project

Gets an existing project by the project id. If the project id value is not specified the call will retrieve the default Contensis instance project.

***get(id?: string): Promise&lt;Project&gt;***

### Returns
A Promise that will resolve with a [Project](/model/project.md) object.

### Example

```js
client.projects.get('website')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
