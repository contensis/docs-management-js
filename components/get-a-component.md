---
description: A component determines a reusable schema added to content types which entries are then created from.
---
# Components

A component determines a reusable schema added to content types which entries are then created from. Components contain a list of fields just like content types, and allow for a standardized schema for modelling content.[Find out more about components on ZenHub](https://zenhub.zengenti.com/Contensis/12.0/kb/content-types-and-entries/components/components-overview.aspx)

## Get a component

Gets an existing component by the component id or by passing a [ComponentGetOptions](/model/component-get-options.md) object as an argument.

 ***get(idOrOptions: string | ComponentGetOptions): Promise&lt;Component&gt;***

### Returns
A Promise that will resolve with a [Component](/model/component.md) object.

### Example

```js
client.components.get('address')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});

client.components.get({
    id: 'address',
    versionStatus: 'published'
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});

client.components.get({
    id: 'address',
    version: '1.2'
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});```
