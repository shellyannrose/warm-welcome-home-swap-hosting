# Update (PUT) the room or area for a task

Use the `host_id`, `guest_id`, and prep-checks `id` to update the room or area for a task.

## URL

```shell

{PUT}{server_url}/prep-checks?host_id={value}&guest_id={value}&id={value}
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the host id in the hosts resource |
| `guest_id` | Number |Refers to the guest id in the guests resource |
| `id` | Number | Service-generated unique ID for the task in the prep-checks resource |

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body

**Important** The request body replaces all the current properties of the task, except the unique IDs. For properties that you do not want to change, you must use their current values in the request body.

```js
[
    {
      
      "title": "Move car",
      "room-area": "Garage",
      "due-date": "2024-09-03",
      "warning": "-72"
    }
]
```

## Return body

The following example shows the response if the `host_id` is 3, `guest_id` is 3, and prep-checks `id` is 4. The title value changed as well.

```js
[
    {
      "host_id": 3,
      "guest_id": 4,
      "title": "Move car",
      "room-area": "Garage",
      "due-date": "2024-09-03",
      "warning": "-72",
      "id": 4
    }
]
```

**Note** You can use a similar request to update the other properties. Just replace the parameters and values in the request body.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated and returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
