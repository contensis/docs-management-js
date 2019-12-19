---
description: Updates an existing project resource.
---
## Update a project

Updates an existing project resource.

***update(project: Project): Promise&lt;Project&gt;***

### Returns
A Promise that will resolve with a [Project](/model/project.md) object.

### Example

```js
client.projects.update({
    "description": "A source of movie and TV series in multiple languages",    
    "supportedLanguage": [
        "fr-FR",
        "de-DE",
        "en-US"
    ]
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```

### Remarks

It is not possible to update the Id once you've created a project.
