---
description: Gets the groups as direct child members of the group
---

# Get child group membership by group id

Gets the direct child group members of the group.

***getChildGroupsByGroupId(groupId: string): Promise&lt;PagedList&lt;Group&gt;&gt;***

## Example
```js
let groupId = "4b262379-5bbe-421e-a429-f6e2ab5a849b";

client.security.groups.getChildGroupsByGroupId(groupId)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```
---

# Get child group membership by group name

Gets the direct child group members of the group.

***getChildGroupsByGroupName(groupName: string): Promise&lt;PagedList&lt;Group&gt;&gt;***

## Example
```js
let groupName = "Test Users";

client.security.groups.getChildGroupsByGroupName(groupName)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```
