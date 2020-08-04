---
description: A child group can be removed from a group.
---

# Remove a child group from a group

A child group can be removed from a group by using the following method: 

***removeChildGroup(groupId: string, childGroupId: string): Promise&lt;void&gt;***

## Example

```js
const groupId = "89CEE207-6F12-4D27-8693-B7693766A82D";
const childGroupId = "F8B27A8F-F1E5-48EF-A5E6-19A791030C0A";
client.security.groups.removeChildGroup(groupId, childGroupId)
    .then(result => {
        console.log('API call was successful');              
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```
