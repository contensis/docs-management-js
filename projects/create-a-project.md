---
description: Creates a new project resource.
---
## Create a project

Creates a new project resource from a [Project](/model/project.md) object passed as an argument.

***create(project: Project): Promise&lt;Project&gt;***

### Returns
A Promise that will resolve with a [Project](/model/project.md) object.

### Example

```js
client.projects.create({
    "id": "movieDb",
    "name": "Movie database",
    "description": "A source of movie and TV series",
    "primaryLanguage": "en-GB",
    "supportedLanguage": [
        "fr-FR",
        "de-DE"
    ]
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```

### Validations

#### Non-unique id

A project must have a unique id. If you attempt to create a project with an id which is already in use you will get the following response.

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors creating the project",
    "data": [
        {
            "field": "",
            "message": "A project with this Id already exists"
        }
    ],
    "type": "Validation"
}
```

#### Primary language is required

A project must have a primary language defined. If you attempt to create a project without specifying a primary language you will get the following response.

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors creating the project",
    "data": [
        {
            "field": "Project",
            "message": "The primary language code is not valid"
        }
    ],
    "type": "Validation"
}
```

### Remarks

If the *primaryLanguage* value is not included in the *supportedLanguages* array then it will automatically be added by the service when the project is created.
