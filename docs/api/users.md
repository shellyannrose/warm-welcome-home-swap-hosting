---
layout: page
---
# `users` resource

Base endpoint

```shell
{server_url}/users
```

Contains information about the users (hosts) of the service. To use the service, the host must register for it.

**Note** All properties are required, unless identfied as optional.

## Resource properties

Sample `users` resource

```js

{
    "last_name": "Smith",
    "first_name": "Wallace",
    "email": "w.smith@example.com",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | Number | Service-generated unique ID for the host |
| `last_name` | String | Host’s last name |
| `first_name` | String | Host’s first name|
| `email` | String |Host’s email address |

## Operations

The `users` resource supports the operations below.

## CREATE (POST)

* [Add new host to service](../api/users_CRUDref/create-add-new-host.md)

## READ (GET)

* [Get all hosts](../api/users_CRUDref/get-all-hosts.md)
* [Get host by id](../api/users_CRUDref/get-host-by-id.md)
* [Get host by last name](../api/users_CRUDref/get-host-by-last-name.md)

## UPDATE (PUT/PATCH)

* [Update (PUT) a host's first name by id](../api/users_CRUDref/update-put-host-firstname-by-id.md)
* [Update (PATCH) a host's email by id](../api/users_CRUDref/update-patch-host-email-by-id.md)

## DELETE (DELETE)

* [Remove host from service by id](../api/users_CRUDref/delete-host-by-id.md)
