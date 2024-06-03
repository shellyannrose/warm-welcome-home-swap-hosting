# Find the due date of a task for a guest

Use the host's `host_id` and the guest's `guest_id` and list the due date of a task for a guest.

## URL

```shell

{GET}{server_url}/prep-checks/{host_id}/{guest_id}/{id}/due-date
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

The following example shows the response for a host whose `host_id` is 1. The `guest_id` is 2, the task id is 2.

```js
[
    {
      "host_id": 1,
      "guest_id": 2,
      "title": "Dust, vacuum, mop",
      "room-area": "Whole house",
      "due-date": "2024-09-04",
      "warning": "-24",
      "id": 2
    }
  ]
```

**Note** You can use a request like this to find all the properties for a task. Just replace the three parameters in the curly braces {} in the request URL. Then change the final parameter.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
