---
description: Updates an entry resource.
---
# Update an entry

Updates an entry resource.

***update(entry: Entry): Promise&lt;Entry&gt;***

## Returns

A Promise that will resolve with a [Entry](/model/entry.md) object.

## Example

```js
existingEntry['title'] = 'Back to the Future';

client.entries.update(existingEntry)
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
  });
```

## Versioning

Contensis uses an optimistic concurrency versioning model. Rather than checking out entries and locking them we allow concurrent updating of entries. At the point in which you update an entry the version you pass in is checked to make sure it is the latest and no one else has created a newer version. If the version you pass in is the latest version then the entry will get updated. If you pass in a version which isn't now the latest then you will get the following response.

```json
{
    "logId": "00000000-0000-0000-0000-000000000000",
    "message": "There are validation errors updating the entry",
    "data": [
        {
            "field": "Entry.Variations.Values[0].entryVariation",
            "message": "The entry variation is not the latest"
        }
    ],
    "type": "Validation"
}
```
