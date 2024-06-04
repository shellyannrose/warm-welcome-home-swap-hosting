# Get a list of all house guests arrival dates

Get a list of all arrival dates for all the host's guests.

## URL

```shell

{GET}{server_url}/guests/{host_id}/arrival-date
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body


The following example shows the response for a host whose `host_id` is 1.

```js
[
    {
      "host_id": 1,
      "arrival-date": "2024-08-12T17:00"
    },
    
    {
      "host_id": 1,
      "arrival-date": "2024-09-05T13:00"
    }
  ]
```


**Note** You can use a request like this to find all the `departure-date` values for any host. To do that, change the parameter in the curly braces {} after the resource name in the request URL. Then change the final parameter after the forward slash in the URL.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
