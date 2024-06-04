# Remove a specific task for a guest from the host's account

Use the host's `host_id` and the guest's `guest_id` and remove a task for a guest.

## URL

```shell

{DELETE}{server_url}/prep-checks/{host_id}/{guest_id}/{id}

```

**Important** Use caution when you create a DELETE request.  If you do not provide an `id` parameter, you will remove all tasks for a guest from a host's account.

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the host id in the hosts resource |
| `guest_id` | Number |Refers to the guest id in the guests resource |
| `id` | Number | Service-generated unique ID for a task in the prep-checks resource|

## Request headers

None

## Request body

None

## Return body

The following example shows the response if the `host_id` value is 2, the `guest_id` is 3, and the `id` value is 3. The task for this guest is no longer in the host's account.

```js
[
    {
      "host_id": 2,
      "guest_id": 3,
      "title": "Leave welcome treats for guests",
      "room/area": "Kitchen",
      "due date": "2024-08-06",
      "warning": "-4",
      "id": 3
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Action completed successfully |
| 202 | Accepted| Action has been queued |
| 204 | No Content| Action has been performed, but the response does not include an entity |
| 404 | Error | Specified house guest record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
