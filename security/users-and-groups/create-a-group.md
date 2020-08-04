---
description: Creates a new group resource
---

# Create a group

Creates a new group resource from a [Group](/model/group.md) object passed as an argument.

 ***create(group: Group): Promise&lt;Group&gt;***

## Remarks

Only a member of the *System Administrators* group can create a group resource.

## Example

```js
let group = {    
    "name": "Paper Street Soap Company",
    "Description": "Employees of the Paper Street Soap Company", 
    "type": "contensis",
    "custom" : {
        "clientId": "PSSC"
    }
};

client.security.groups.create(group)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call fetch error: ', error);        
    });
```
