---
description: A EntryListOptions is a structure that is used to describe details for requesting entries.
---
# EntryListOptions

A EntryListOptions is a structure that is used to describe details for requesting entries.

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| contentTypeId | string | | The content type identifier. |
| versionStatus | string | | The version status, either *published* or *latest*. The default is *latest*. |
| pageOptions | object | [PageOptions](/model/page-options.md) | The page options. |
| order | string[] |  | A array of field Ids to order the results by. Prefix field Id with - for descending order. |
| language | string | [LanguageCode](/key-concepts/localization.md) | The variation language code. |
