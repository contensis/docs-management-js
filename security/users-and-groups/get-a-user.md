---
description: A user resource can be retrieved by it's GUID identifier
---

# Get a user by id

A user resource can be retrieved by it's GUID identifier.

 ***getById(userId: string): Promise&lt;User&gt;***

## Returns
A Promise that will resolve with a [User](/model/user.md) object.

## Example

```js
client.security.users.getById('bd8f92eb-d137-49d8-9e7a-560078a8a530')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call error: ', error);      
});
```

---

# Get a user by username

A user resource can be retrieved by its username.

***getByUsername(username: string): Promise&lt;User&gt;***

## Example

```js
client.security.users.getByUsername('testuser')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call error: ', error);      
});
```

---

# Get a user by email

A user resource can be retrieved by it's email address.

***getByEmail(email: string): Promise&lt;User&gt;***

## Example

```js
client.security.users.getByEmail('testuser@test.com')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call error: ', error);      
});
```
