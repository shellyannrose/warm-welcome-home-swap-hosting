# Get a list of all house guests arrival dates

Get a list of all arrival dates for all the host's guests.

## URL

```shell

{GET}{server_url}/house-exchanges/{user_id}/arrival-date
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

The following example shows the response for a host whose `user_id` is 1.

```js
[
    {
      "user_id": 1,
      "arrival-date": "2024-08-12T17:00"
    },
 {
      "user_id": 1,
      "arrival-date": "2024-09-05T13:00"
    }
  ]
```

**Note** You can use a similar request to find all the `departure-date` values. Just replace the parameter in the curly braces {} at the end of the URL in the GET request

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
