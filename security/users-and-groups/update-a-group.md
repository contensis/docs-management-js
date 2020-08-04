---
description: Updates a group resource.
---

# Update a group

Updated a group resource from a [Group](/model/group.md) object passed as an argument.

 ***update(group: Group): Promise&lt;Group&gt;***

## Remarks
Only a member of the *System Administrators* group can update a group resource.

## Example

```js
let group = {    
    "id": "4b262379-5bbe-421e-a429-f6e2ab5a849b",
    "name": "Paper Street Soap Company",
    "Description": "Employees of the Paper Street Soap Company", 
    "type": "contensis",
    "custom" : {
        "clientId": "PSSC"
    }
};

client.security.groups.update(group)
    .then(result => {
        console.log('API call result: ', result);
    })
    .catch(error => {
        console.log('API call error: ', error);        
    });
```
