---
description: Creates a new component resource.
---

# Create a component

Creates a new component resource  from a [Component](/model/component.md) object passed as an argument.

***create(component: Component): Promise&lt;Component&gt;***

## Returns

A Promise that will resolve with a [Component](/model/component.md) object.

## Example

```js
let newComponent = {
    "id": "address",
    "projectId": "movieDb",
    "name": {
        "en-GB": "Address"
    },
    "description": {
        "en-GB": "An address component"
    },    
    "fields": [
        {
            "id": "firstLine",
            "name": {
                "en-GB": "First line"
            },
            "dataType": "string",
            "editor": {
                "id": "text",
                "instructions": {
                    "en-GB": "The first line of address"
                },
                "properties": {
                    "placeholderText": {
                        "en-GB": "Enter the first line of address"
                    }
                }
            }
        },
        {
            "id": "postCode",
            "name": {
                "en-GB": "Post code"
            },
            "dataType": "string",
        }
    ]
};

client.components.create(newComponent)
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
  });
```

## Validations

| Type | Description |
|-|-|
| Project does not exist | A project must exist to be able to create components. |
| Non-unique id | The component must be unique for the project. |
