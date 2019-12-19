---
description: An entry definition in the Management API contains a mixture of standard properties and properties that have been defined by the content type that an entry is based on.
---
# Entries

An entry definition in the Management API contains a mixture of standard properties and properties that have been defined by the content type that an [entry](https://zenhub.zengenti.com/Contensis/11.3/kb/content-types-and-entries/entries/entries-overview.aspx) is based on.

## Get an entry

Gets an existing entry by its id or by passing an [EntryGetOptions](/model/entry-get-options.md) object as an argument.

 ***get(idOrOptions: string | EntryGetOptions): Promise&lt;Entry&gt;***

### Returns
A Promise that will resolve with an [Entry](/model/entry.md) object.

### Example

```js
client.entries.get('bd8f92eb-d137-49d8-9e7a-560078a8a530')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});

client.entries.get({
    id: 'bd8f92eb-d137-49d8-9e7a-560078a8a530',
    versionStatus: 'published'
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});

client.entries.get({
    id: 'bd8f92eb-d137-49d8-9e7a-560078a8a530',
    version: '1.2',
    language: 'fr-FR'
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
