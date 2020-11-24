---
description: The Management API allows you to create and manage entries within Contensis.
---

# Contensis JS Management API

## Introduction

The Management API allows you to create and manage entries within Contensis.
Our primary aim with this version of the API is to enable you to easily import/integrate content from other systems.

The API is a RESTful service to ensure maximum compatibility, delivering content as JSON and resource files (assets) as text or binary files. The life-cycle of  [content is controlled by workflow](/key-concepts/workflow.md) which can be controlled by invoking events. We currently provide [.NET](https://developer.zengenti.com/contensis/api/management/dotnet/) and [JS](https://developer.zengenti.com/contensis/api/management/js/) client API wrappers to simplify using the API.

## Key concepts

- [API instantiation](key-concepts/api-instantiation.md)

### Projects

- [Get a project](/projects/get-a-project.md)      
- [Create a project](/projects/create-a-project.md)
- [Update a project](/projects/update-a-project.md)
- [List projects](/projects/list-projects.md)      
- [Delete a project](/projects/delete-a-project.md)

### Content types

- [Get a content type](/content-types/get-a-content-type.md)
- [Create a content type](/content-types/create-a-content-type.md)
- [Update a content type](/content-types/update-a-content-type.md)
- [List content types](/content-types/list-content-types.md)
- [Delete a content type](/content-types/delete-a-content-type.md)
- [Publish a content type](/content-types/invoking-workflow.md)

### Components

- [Get a component](/components/get-a-component.md)
- [Create a component](/components/create-a-component.md)
- [Update a component](/components/update-a-component.md)
- [Add a component to a content type](/components/add-a-component-to-a-content-type.md)
- [List components](/components/list-components.md)
- [Delete a component](/components/delete-a-component.md)
- [Publish a component](/components/invoking-workflow.md)

### Entries

- [Get an entry](/entries/get-an-entry.md)
- [Create an entry](/entries/create-an-entry.md)
- [Update an entry](/entries/update-an-entry.md)
- [List entries](/entries/list-entries.md)
- [Delete an entry](/entries/delete-an-entry.md)
- [Invoking workflow event](/entries/invoking-workflow.md)

### Nodes

- [Get the root node](/nodes/get-root-node.md)           
- [Get a node](/nodes/get-a-node.md)                     
- [Get nodes by entry id](/nodes/get-nodes-by-entryid.md)
- [Get a node's children](/nodes/get-nodes-children.md)  
- [Create a node](/nodes/create-a-node.md)               
- [Update a node](/nodes/update-a-node.md)               
- [Move a node](/nodes/move-a-node.md)                   
- [Delete a node](/nodes/delete-a-node.md)               
- [Order nodes](/nodes/order-nodes.md)                   

### Users and groups
* [Get a user](security/users-and-groups/get-a-user.md)
* [List users](security/users-and-groups/list-users.md)
* [Create a user](security/users-and-groups/create-a-user.md)
* [Update a user](security/users-and-groups/update-a-user.md)
* [Delete a user](security/users-and-groups/delete-a-user.md)
* [Update a user password](security/users-and-groups/update-user-password.md)
* [Suspend a user](security/users-and-groups/suspend-a-user.md)
* [Unlock a user](security/users-and-groups/unlock-a-user.md)
* [Unsuspend a user](security/users-and-groups/unsuspend-a-user.md)
* [Check group membership](security/users-and-groups/check-group-membership.md)
* [Get a group](security/users-and-groups/get-a-group.md)
* [List groups](security/users-and-groups/list-groups.md)
* [Create a group](security/users-and-groups/create-a-group.md)
* [Update a group](security/users-and-groups/update-a-group.md)
* [Delete a group](security/users-and-groups/delete-a-group.md)
* [Get users in group](security/users-and-groups/get-users-in-group.md)
* [Get user group membership](security/users-and-groups/get-user-group-membership.md)
* [Get child groups in group](security/users-and-groups/get-groups-in-group.md)
* [Add user to a group](security/users-and-groups/add-user-to-group.md)
* [Remove user from a group](security/users-and-groups/remove-user-from-group.md)
* [Add child group to a group](security/users-and-groups/add-group-to-group.md)
* [Remove child group from a group](security/users-and-groups/remove-group-from-group.md)

### Roles

- [Get a role](/roles/get-a-role.md)      
- [Create a role](/roles/create-a-role.md)
- [Update a role](/roles/update-a-role.md)
- [List roles](/roles/list-roles.md)      
- [Delete a role](/roles/delete-a-role.md)

### Permissions

- [Overview](/permissions/overview.md)
- [Get permissions for a resource](/permissions/get-permissions-for-a-resource.md)
- [Get authorization for a resource action](/permissions/get-authorization-for-a-resource-action.md)
