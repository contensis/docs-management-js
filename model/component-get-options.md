---
description: A ComponentGetOptions is a structure that is used to describe details for requesting a content type.
---
# ComponentGetOptions

A ComponentGetOptions is a structure that is used to describe details for requesting a component.

## Properties

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| id | string |  | The component identifier. |
| versionStatus | string |  | The version status, either *published* or *latest*. The default is *latest*. |
| version | number | {Major}.{Minor} | The version number of the resource. |


## Remarks

If a specific *version* value has been provided then the *versionStatus* value will be ignored.
