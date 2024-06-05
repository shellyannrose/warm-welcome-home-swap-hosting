---
layout: page
---
# `prep-checks` resource

Base endpoint

```shell
{server_url}/prep-checks
```

Contains information about the tasks the host must completed befora a guest arrives.

**Note** All properties are required, unless identified as optional.

## Resource properties

Sample `prep-checks` resource

```js

{
    "host_id": 1,
    "guest_id": 1,
    "title": "Bed linen change",
    "room-area": "Bedrooms",
    "due-date": "2024-08-10",
    "warning": "-12",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the host id in the hosts resource |
| `guest_id` | Number |Refers to the guest id in the guests resource |
| `title` | String |The name of the task |
| `room-area` | String|The part of the home that requires the task |
| `due-date` | String | The date the host chooses to finish the task |
| `warning` | Number |The number of minutes relative to the due date to alert the host to finish the task. This is normally a negative number to alert the host before the due date. |
| `id` | Number | Service-generated unique ID for the prep-checks task |

## Operations

The `prep-checks` resource supports the operations below.

## CREATE (POST)

* [Add a task to prepare for a guest](../api/prep_check_CRUDref/create-prep-check-task.md)

## READ (GET)

* [Get all tasks for a host](../api/prep_check_CRUDref/get-all-prep-check-tasks.md)
* [Get tasks for a specific due date](../api/prep_check_CRUDref/get-prep-check-tasks-by-due-date.md)

## UPDATE (PUT/PATCH)

* [Update (PATCH) a task's warning time](../api/prep_check_CRUDref/update-patch-warning-by-id.md)
* [Update (PUT) a room or area for a task](../api/prep_check_CRUDref/update-put-room-area-by-guest-id.md)

## DELETE (DELETE)

* [Remove a task for a guest](../api/prep_check_CRUDref/delete-prep-check-task-by-id.md)
