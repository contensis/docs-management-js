## Delete a role

Deletes a role by its id.

***delete(id: string): Promise&lt;void&gt;***

### Example

```js
client.roles.delete('71f73a9b-2a13-4d63-bcc1-e8ee5047b01c')
  .then(result => {      
    console.log('API call was successful');              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```

### Validations

#### Project does not exist

Roles are project specific. If you attempt to delete a role in a project which does not exist you will get the following response. 

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors deleting the role",
    "data": [
        {
            "field": "projectId",
            "message": "The project does not exist"
        }
    ],
    "type": "Validation"
}
```

#### Role does not exist

If you attempt to delete a role which does not exist you will get the following response. 

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors deleting the role",
    "data": [
        {
            "field": "projectId",
            "message": "The role with id '71f73a9b-2a13-4d63-bcc1-e8ee5047b01c' does not exist"
        }
    ],
    "type": "Validation"
}
```

#### Insufficient permissions to delete a role

In order to delete a role you must be a member of the "System Administrators" user group. If you do not have permission to delete a role you will get the following response.

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors deleting the role",
    "data": [
        {
            "message": "Access denied"
        }
    ],
    "type": "Validation"
}
```