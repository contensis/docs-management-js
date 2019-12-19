---
description: A EntryGetOptions is a structure that is used to describe details for requesting an entry.
---
# EntryGetOptions

A EntryGetOptions is a structure that is used to describe details for requesting an entry.

## Properties

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| id | string |  | The content type identifier. |
| versionStatus | string |  | The version status, either *published* or *latest*. The default is *latest*. |
| version | number | {Major}.{Minor} | The version number of the resource. |
| language | string | [LanguageCode](/key-concepts/localization.md) | The variation language code.     

## Remarks

If a specific *version* value has been provided then the *versionStatus* value will be ignored.
