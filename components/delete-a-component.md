---
description: Deletes a component from a specific project.
---

# Delete a component

Deletes a component from a specific project.

***delete(id: string): Promise&lt;void&gt;***

## Returns
A Promise that will resolve with an empty object.

## Example

```js
client.components.delete('address')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```

## Validations

### Deleting a component which is in use

If a component is in use within a content type then it can't be deleted. If you attempt to delete a component which is in use you will get the following response.

```json
{
    "logId": "6eda131e-c8eb-44dc-8665-ae3a8b1815d8",
    "message": "There are validation errors deleting the component",
    "data": [
        {
            "field": "",
            "message": "The component cannot be deleted as it is in use in one or more content types"
        }
    ],
    "type": "Validation"
}
```
