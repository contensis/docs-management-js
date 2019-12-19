---
description: Workflow events can be invoked for a specific content type.
---
# Invoking workflow for a content type

Workflow events can be invoked for a specific content type.

 ***invokeWorkflow(contentType: ContentType, event: string, data?: any): Promise&lt;ContentType&gt;***

## Parameters

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| contentType | object | [ContentType](/model/content-type.md) | The content type object. |
| event | string | | The event type, currently the only one supported for content types is *publish*. |
| data? | object | | The optional event data. |

## Returns
A Promise that will resolve with a [ContentType](/model/content-type.md) object.

## Example

```js
client.contentTypes.invokeWorkflow(existingContentType, 'publish')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
