---
description: A UserListOptions is a structure that is used to describe details for requesting users.
---
# UserListOptions

A *UserListOptions* is a structure that is used to describe details for requesting users.

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| q? | string | | An simple query to perform a 'contains' search over users firstname, surname, username and email. |
| pageOptions? | object | [PageOptions](/model/page-options.md) | The page options. |
| order? | string[] | | An array of properties to order the results by. <br>Prefix property with - for descending order. |
