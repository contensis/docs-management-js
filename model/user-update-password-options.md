---
description: A UserUpdatePasswordOptions is a structure that is used to describe details for updating a user password.
---
# UserUpdatePasswordOptions

A *UserUpdatePasswordOptions* is a structure that is used to describe details for updating a user password

| Name | Type | Description |
|:-|:-|:-|:-|
| userId | string | The id of the user. |
| new | string | The new password for the user. |
| existing? | string | If the user does not have administrative privileges the existing password need to be specified. |
