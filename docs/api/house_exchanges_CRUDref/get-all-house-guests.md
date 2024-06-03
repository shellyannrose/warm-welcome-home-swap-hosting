# Get a list of all house guests for a specific host

Use host's `user_id` to get a list of all the guests for the host.

## URL

```shell

{GET}{server_url}/house-exchanges/{user_id}
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

The following example response shows the guests for a host whose `user_id` is 2.

```js
[
    {
      "user_id": 2,
      "arrival-date": "2024-08-07T11:00",
      "departure-date": "2024-08-14T12:00", 
      "guest-names": "Pat",
      "last-name-primary": "Brent",
      "number-of-guests ": "2",
      "type-of-exchange": "Guest Points",  
      "id": 3
    },
  ]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | The requested resource does not exist |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
