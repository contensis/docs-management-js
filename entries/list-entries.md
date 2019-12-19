---
description: Lists entries by content type.
---
# List entries by content type

Lists entries by content type id or by passing an [EntryListOptions](/model/entry-list-options.md) object as an argument.

***list(contentTypeIdOrOptions: string | EntryListOptions): Promise&lt;PagedList&lt;Entry&gt;&gt;***

## Returns

A Promise that will resolve with a [PagedList](/model/paged-list.md) that contains an array of [Entry](/model/entry.md) objects.

## Example

```js
client.entries.list({    
    contentType: 'movie',
    versionStatus: 'published',
    language: 'fr-FR',
    order: ['entryTitle'],
    pageOptions: {      
      pageSize: 50
    }    
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
