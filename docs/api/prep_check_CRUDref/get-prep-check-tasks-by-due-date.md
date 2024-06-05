# Find all tasks for a due date

Use the `due-date` to list the tasks for that date.

## URL

```shell

{GET}{server_url}/prep-checks?due-date=2024-09-04
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

The following example shows the response for all tasks due by September 4, 2024.

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

**Note** You can use a request like this to find tasks by another property's value. Just replace the parameter and value in the request URL.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
