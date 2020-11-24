---
description: Unsuspend a user.
---

# Unsuspend a user

A user can be unsuspended using the following call:

 ***unsuspendUser(userId: string): Promise&lt;void&gt;***

## Remarks
The *userId* can be username, email address or a GUID identifier.

If the user is not found then an exception with a *404 Not found* is thrown.  
If there are no permissions to unsuspend a user then an exception with a *403 Forbidden* status is thrown.  

## Example

```js
client.security.users.unsuspendUser("4b262379-5bbe-421e-a429-f6e2ab5a849b")
    .then( result => {
        console.log('API call was successful');
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```
