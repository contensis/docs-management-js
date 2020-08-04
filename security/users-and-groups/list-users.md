---
description: User resources can be retrieved as a paged list
---

## List users

User resources can be retrieved as a paged list by passing an optional [UserListOptions](/model/user-list-options.md) object as an argument.

***list(options?: UserListOptions): Promise&lt;PagedList&lt;User&gt;&gt;***

## Returns

A Promise that will resolve with a [PagedList](/model/paged-list.md) that contains an array of [User](/model/user.md) objects.

## Example

```js
client.security.users.list({
        q: 'mycompany.com',
        pageOptions: { pageIndex: 1, pageSize: 5 },
        order: ['userName']
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call error: ', error);      
});
```
