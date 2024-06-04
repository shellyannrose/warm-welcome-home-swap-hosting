# Add a task to prepare for a guest

Use the host's `host_id` and the guest's `guest_id` and create a new task for a guest.

## URL

```shell

{POST}{server_url}/prep-checks/{host_id}/{guest_id}
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the host id in the hosts resource |
| `guest_id` | Number |Refers to the guest id in the guests resource |
| `title` | String |The name of the task |
| `room/area` | String|The part of the home that requires the task |
| `due-date` | String | The date the host chooses to finish the task |
| `warning` | Number |The number of minutes relative to the due date to alert the host to finish the task. This is normally a negative number to alert the host before the due date |

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body

```js
[
   {
    "host_id": 1,
    "guest_id": 1,
    "title": "Bed linen change",
    "room/area": "Bedrooms",
    "due date": "2024-08-10",
    "warning": "-12"
        
   }
]
```

## Return body

The following example shows the response for a host whose `host_id` is 1 and `guest_id` is 1. The information should be the same as what you placed in the request body. The response should include a new prep-checks' service-generated id for the task.

```js
[
     {
      "host_id": 1,
      "guest_id": 1,
      "title": "Bed linen change",
      "room/area": "Bedrooms",
      "due date": "2024-08-10",
      "warning": "-12",
      "id": 1 
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | User data created successfully |
| 500 | Internal server error | Invalid JSON |
| 404 | Error | The requested resource does not exist |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
