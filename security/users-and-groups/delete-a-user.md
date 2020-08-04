---
description: Deletes a user resource.
---

# Delete a user

Deletes a user by its id.

***delete(userId: string): Promise&lt;void&gt;***

## Remarks

Only a member of the *System Administrators* group can delete a user resource.

# Example 

```js
let userId = "4b262379-5bbe-421e-a429-f6e2ab5a849b";

client.security.users.delete(userId)
    .then(result => {
        console.log('API call was successful');
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```