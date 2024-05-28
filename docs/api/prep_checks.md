---
layout: page
---
# `prep-checks` resource

Base endpoint

```shell
{server_url}/prep-checks
```

Contains information about the tasks the host must completed befora a guest arrives.

**Note** All properties are required, unless identfied as optional.

## Resource properties

Sample `prep-checks` resource

```js

{
    "user_id": 1,
    "exchange_id": 1,
    "title": "Bed linen change",
    "room/area": "Bedrooms",
    "due date": "2024-08-10",
    "warning": "-12",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | Refers to the host id in the users resource |
| `exchange_id` | Number |Refers to the house-exchanges id in the house-exchanges resource |
| `title` | String |The name of the task |
| `room/area` | String|The part of the home that requires the task |
| `due-date` | String | The date the host chooses to finish the task |
| `warning` | Number |The number of minutes relative to the due date to alert the host to finish the task. This is normally a negative number to alert the host before the due date. |
| `id` | Number | Service-generated unique ID for the prep-check task |

## Operations

The `prep-checks` resource supports the operations below.

## CREATE (POST)

* [Add a task to prepare for a guest](tbd)

## READ (GET)

* [Get all prep-check tasks](tbd)
* [Get prep-check task by id](tbd)
* [Get prep-check task by exchange_id](tbd)
* [Get all prep-check titles](tbd)
* [Get prep-check title by id](tbd)
* [Get prep-check title by exchange_id](tbd)
* [Get all room/area info](tbd)
* [Get room/area info by id](tbd)
* [Get room/area info by exchange_id](tbd)
* [Get all due dates](tbd)
* [Get a due date by id](tbd)
* [Get a due date by exchange_id](tbd)
* [Get all warning numbers](tbd)
* [Get a warning number by id](tbd)
* [Get a warning number by exchange_id](tbd)

## UPDATE (PUT/PATCH)

* [Update a title by id](tbd)
* [Update a title by exchange_id](tbd)
* [Update a room/area by id](tbd)
* [Update a room/area by exchange_id](tbd)
* [Update a due date by id](tbd)
* [Update a due date by exchange_id](tbd)
* [Update a warning by id](tbd)
* [Update a warning by exchange_id](tbd)

## DELETE (DELETE)

* [Remove all prep-check tasks](tbd)
* [Remove a prep-check task by id](tbd)
* [Remove all prep-check tasks by exchange_id](tbd)
* [Remove a prep-check task by exchange_id](tbd)
