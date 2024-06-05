# Update (PATCH) the warning time for a task

Use the `host_id`, `guest_id`, and prep-checks `id` to update the warning minutes for a task for a guest.

## URL

```shell

{PATCH}{server_url}/prep-checks?host_id={value}&guest_id={value}&id={value}
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

**Important** This request only changes the properties that you place in the request body. All other properties stay the same.

```js
[
    {
      "warning": -7      
    }
]
```

## Return body

The following example shows the response if the `host_id` is 2, `guest_id` is 3, and prep-checks `id` is 3.

```js
[
    {
      "host_id": 2,
      "guest_id": 3,
      "title": "Leave welcome treats for guests",
      "room-area": "Kitchen",
      "due-date": "2024-08-06",
      "warning": "-7",
      "id": 3
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
