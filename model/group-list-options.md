---
description: A GroupListOptions is a structure that is used to describe details for requesting groups.
---
# GroupListOptions

A *GroupListOptions* is a structure that is used to describe details for requesting groups.

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| q? | string | | An simple query to perform a 'contains' search over group names. |
| pageOptions? | object | [PageOptions](/model/page-options.md) | The page options. |
| order? | string[] | | An array of properties to order the results by. <br>Prefix property with - for descending order. |
