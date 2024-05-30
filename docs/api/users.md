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

* [Add new host to service](/tutorials/create-add-new-host.md)

## READ (GET)

* [Get all hosts](tbd)
* [Get host by id](tbd)
* [Get host by last_name](tbd)
* [Get host by first_name](tbd)
* [Get host by email](tbd)

## UPDATE (PUT/PATCH)

* [Update a host's last name](tbd)
* [Update a host's first name](tbd)
* [Update a host's email](tbd)

## DELETE (DELETE)

* [Remove host from service by id](tbd)
