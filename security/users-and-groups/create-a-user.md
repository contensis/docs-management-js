---
description: Creates a new user resource.
---

# Create a user

Creates a new user resource from a [User](/model/user.md) object passed as an argument.

 ***create(user: User): Promise&lt;User&gt;***

## Remarks

Only a member of the *System Administrators* group can create a user resource.

## Example

```js
let user = {    
    "userName": "tdurden",
    "email": "t.turden@fightclub.com",
    "firstname": "Tyler",
    "lastname": "Durden",
    "timezone": "America/New_York",
    "language": "en-US",
    "custom": {
        "department": "Soap sales"
    },
    "credentials": {
        "password": "pr0j3ctM4yh3m"
    }
};

client.security.users.create(user)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call fetch error: ', error);        
    });
```
