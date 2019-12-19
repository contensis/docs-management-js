---
description: Workflow events can be invoked for a specific component.
---
# Invoking workflow for a component

Workflow events can be invoked for a specific content type.

 ***invokeWorkflow(component: Component, event: string, data?: any): Promise&lt;Component&gt;***

## Parameters

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| contentType | object | [Component](/model/component.md) | The component object. |
| event | string | | The event type, currently the only one supported for components is *publish*. |
| data? | object | | The optional event data. |

## Returns
A Promise that will resolve with a [Component](/model/component.md) object.

## Example

```js
client.components.invokeWorkflow(existingComponent, 'publish')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```