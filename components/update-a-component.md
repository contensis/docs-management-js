---
description: Updates an existing component resource.
---

# Update a component

Updates an existing component resource.


***update(component: Component): Promise&lt;Component&gt;***

## Returns

A Promise that will resolve with a [Component](/model/component.md) object.

## Example

```js
existingComponent.description['en-GB'] = 'UK address component';

client.components.update(existingComponent)
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
  });
```
