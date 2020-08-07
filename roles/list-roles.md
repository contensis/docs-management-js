## List roles
Role resources can be retrieved as a paged list by passing an optional [PageOptions](/model/page-options.md) object as an argument.

***list(options?: PageOptions): Promise&lt;PagedList&lt;Role&gt;&gt;***

## Returns

A Promise that will resolve with a [PagedList](/model/paged-list.md) that contains an array of [Role](/model/role.md) objects.

## Example

```js
client.roles.list({
        pageIndex: 1, 
        pageSize: 5
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call error: ', error);      
});
```

### Validations

#### Project does not exist

Roles are project specific. If you attempt to list roles in a project which does not exist you will get the following response. 

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors listing the roles",
    "data": [
        {
            "field": "projectId",
            "message": "The project does not exist"
        }
    ],
    "type": "Validation"
}
```

#### Insufficient permissions to list roles

In order to list roles you must be a member of the "System Administrators" user group. If you do not have permission to list roles you will get the following response.

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors listing the roles",
    "data": [
        {
            "message": "Access denied"
        }
    ],
    "type": "Validation"
}
```