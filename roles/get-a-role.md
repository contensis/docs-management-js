## Get a role

Gets a role by its id.

***get(id: string): Promise&lt;Role&gt;***

### Returns
A Promise that will resolve with a [Role](/model/role.md) object.

### Example

```js
client.roles.get('c31111e7-76f7-46dd-93fb-cbf81a853a37')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```


### Validations

#### Project does not exist

Roles are project specific. If you attempt to get a role in a project which does not exist you will get the following response. 

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors getting the role",
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

If you attempt to get a role which does not exist you will get the following response. 

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors getting the role",
    "data": [
        {
            "field": "projectId",
            "message": "The role with id '71f73a9b-2a13-4d63-bcc1-e8ee5047b01c' does not exist"
        }
    ],
    "type": "Validation"
}
```

#### Insufficient permissions to get a role

In order to get a role you must be a member of the "System Administrators" user group. If you do not have permission to get a role you will get the following response.

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors getting the role",
    "data": [
        {
            "message": "Access denied"
        }
    ],
    "type": "Validation"
}
```