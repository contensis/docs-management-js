---
description: A group resource can be retrieved by it's GUID identifier
---

## Get a group by id

A group resource can be retrieved by it's GUID identifier.


 ***getById(groupId: string): Promise&lt;Group&gt;***  

## Returns
A Promise that will resolve with a [Group](/model/group.md) object.

## Example

```js
client.security.groups.getById('bd8f92eb-d137-49d8-9e7a-560078a8a530')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call error: ', error);      
});
```

---

# Get a group by name

A group resource can be retrieved by its name.

***getByName(username: string): Promise&lt;Group&gt;***

## Example

```js
client.security.groups.getByNme('Test Group')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call error: ', error);      
});
```
