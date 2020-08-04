---
description: Group resources can be retrieved as a paged list
---

## List groups

Group resources can be retrieved as a paged list by passing an optional [GroupListOptions](/model/group-list-options.md) object as an argument.

***list(options?: GroupListOptions): Promise&lt;PagedList&lt;Group&gt;&gt;***

## Returns

A Promise that will resolve with a [PagedList](/model/paged-list.md) that contains an array of [Group](/model/group.md) objects.

## Example

```js
client.security.groups.list({
        q: 'Administrators',
        pageOptions: { pageIndex: 1, pageSize: 5 },
        order: ['name']
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call error: ', error);      
});
```
