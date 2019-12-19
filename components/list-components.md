---
description: Gets the components for a project.
---
# List components

Gets the components for a project.

***list(versionStatus?: VersionStatus): Promise&lt;Component[]&gt;***

## Returns

A Promise that will resolve with an array of [Component](/model/component.md) objects.

## Parameters

| Name | Type | Description |
|:-|:-|:-|
| versionStatus | string | The version status, either *published* or *latest*. The default is *latest*. |

## Example

```js
client.components.list('published')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
