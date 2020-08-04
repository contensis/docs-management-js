---
description: Deletes a group resource.
---

# Delete a group

Deletes a group by its id.

***delete(id: string): Promise&lt;void&gt;***

## Remarks

Only a member of the *System Administrators* group can delete a group resource.

# Example 

```js
let groupId = "4b262379-5bbe-421e-a429-f6e2ab5a849b";

client.security.groups.delete(groupId)
    .then(result => {
        console.log('API call was successful');
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```