---
description: Gets the users as direct members of the group
---

# Get group user membership by group id

Gets the users as direct members of the group.

***getUsersByGroupId(groupId: string): Promise&lt;PagedList&lt;User&gt;&gt;***

## Example
```js
let groupId = "4b262379-5bbe-421e-a429-f6e2ab5a849b";

client.security.groups.getUsersByGroupId(groupId)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```
---

# Get group user membership by group name

Gets the users as direct members of the group.

***getUsersByGroupName(groupName: string): Promise&lt;PagedList&lt;User&gt;&gt;***

## Example
```js
let groupName = "Test Users";

client.security.groups.getUsersByGroupName(groupName)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```
