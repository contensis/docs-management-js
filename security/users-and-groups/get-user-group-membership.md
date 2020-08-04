---
description: Gets the groups the user is a member of
---

# Get group membership for a user

Gets the groups the user is a member of by passing the user id or a [UserGroupsOptions](/model/user-group-options.md) object as an argument.

***getUserGroupsuserIdOrOptions: string | UserGroupsOptions): Promise&lt;PagedList&lt;Group&gt;&gt;***

## Example for direct parent groups
```js
let userId = "4b262379-5bbe-421e-a429-f6e2ab5a849b";

client.security.users.getUserGroups(userId)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```

## Example for inherited parent groups

```js
let options = {
    userId: "4b262379-5bbe-421e-a429-f6e2ab5a849b",
    includeInherited: true
};

client.security.users.getUserGroups(options)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```
