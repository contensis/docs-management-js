---
description: Updates a user resource.
---

# Update a user

Updated a user resource from a [User](/model/user.md) object passed as an argument.

 ***update(user: User): Promise&lt;User&gt;***

## Remarks

Only the current user and a member of the *System Administrators* group can update a user resource

## Example

```js
let user = {    
    "userId": "4b262379-5bbe-421e-a429-f6e2ab5a849b",
    "email": "t.turden@test.com",    
    "custom": {
        "department": "Marketing"
    }    
};

client.security.users.update(user)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```
