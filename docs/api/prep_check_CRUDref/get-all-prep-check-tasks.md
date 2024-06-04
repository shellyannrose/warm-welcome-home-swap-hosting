# Get a list of all the tasks for a specific host

Use the host's `host_id` to get a list of all the tasks for a host.

## URL

```shell

{GET}{server_url}/prep-checks/{host_id}
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

The following example response shows all the tasks for a host whose `host_id` is 1.

```js
[
     {
      "host_id": 1,
      "guest_id": 1,
      "title": "Bed linen change",
      "room-area": "Bedrooms",
      "due-date": "2024-08-10",
      "warning": "-12",
      "id": 1
    },
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

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | The requested resource does not exist |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
