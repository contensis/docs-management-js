---
description: Set the node order
---

# Node order

## Set the node order

Sets the node order for the children of a specific parent node and optionally for a language.

***setChildrenOrder(id: string, childrenIds: string[], language?: string): Promise&lt;void&gt;***

### Parameters

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| id | string | | The container node for the children which are being ordered. |
| childrenIds | string[] | | The array of node children ids that are being ordered. |
| language | string | [LanguageCode](/key-concepts/localization.md) | [Optional] The target language that the order is being applied. If no language is specified then the default language order is set. |

### Remarks

The default language order is used for other languages if no language specific order is set.

### Example

The example below is setting the node order specifically for French.

```js
client.nodes.setChildrenOrder(
  '09795671-12d5-486e-8a9d-1c4b8048fbe3',
  ['167ac193-c6ea-4aae-b7ce-68b26152eca5', '936b6e09-05cf-4652-8872-45c9fc99fc2c', '45bfd6a1-e8fb-44e0-a457-bf64cea5ea25'],
  'fr-FR')
  .then(result => {      
    console.log('API call was successful');              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
---

## Remove the node order

Deletes the node order for the children of a specific parent node and optionally for a language.

***deleteChildrenOrder(id: string, language?: string): Promise&lt;void&gt;***

### Parameters

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| id | string |  | The container node for the children which have an order. |
| language | string | [LanguageCode](/key-concepts/localization.md)  | [Optional] The target language that the order is applied. If no language is specified then the default language order is deleted. |

### Example

The example below is deleting the node order specifically for German.

```js
client.nodes.setChildrenOrder(
  '09795671-12d5-486e-8a9d-1c4b8048fbe3',  
  'de')
  .then(result => {      
    console.log('API call was successful');              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```
