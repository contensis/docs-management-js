---
description: Workflow events can be invoked for a specific entry.
---
# Invoking workflow for an entry using the event name and event data

Workflow events can be invoked for a specific entry by passing the event name and the event data.

 ***invokeWorkflow(entry: Entry, event: string, data?: any): Promise&lt;Entry&gt;***

## Parameters

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| entry | object | [Entry](/model/entry.md) | The entry object. |
| event | string | | The event type, as described at [Workflow](/key-concepts/workflow.md) |
| data? | object | | The optional event data. |

## Returns
A Promise that will resolve with an [Entry](/model/entry.md) object.

## Example

```js
client.entries.invokeWorkflow(existingEntry, 'draft.publish')
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```

# Invoking workflow for an entry using the workflow trigger object

Workflow events can be invoked for a specific entry by passing a workflow trigger object. This method allows more flexibility than *invokeWorkflow* as you can omit the language and the version number if not required. You should use this method when you need to unpublish an entry, like in the example below.

 ***invokeWorkflowByTrigger(entry: Entry, workflowTrigger: WorkflowTrigger): Promise&lt;Entry&gt;***

## Parameters

| Name | Type | Format | Description |
|:-|:-|:-|:-|
| entry | object | [Entry](/model/entry.md) | The entry object. |
| workflowTrigger | object | [WorkflowTrigger](/model/workflow-trigger.md) | The workflow trigger object type. |

## Returns
A Promise that will resolve with an [Entry](/model/entry.md) object.

## Example

```js
   client.entries.invokeWorkflowByTrigger(existingEntry, {
    event: 'sysUnpublish',
    language: 'en-GB'
  })
  .then(result => {      
    console.log('API call result: ', result);              
  })
  .catch(error => {
    console.log('API call fetch error: ', error);      
});
```