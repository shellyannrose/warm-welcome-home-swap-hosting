# Update (PUT) guest names

Use the host's `host_id` and the guest's `id` and change the guest names.

## URL

```shell

{PUT}{server_url}/guests/{host_id}/{id}

```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the host id in the hosts resource |
| `id` | Number | Service-generated unique ID for the guests resource |


## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body

**Important** The request body replaces all the current properties of the guest. For properties that you do not want to change, you must use their current values in the request body.

```js
[
    {
      "arrival-date": "2024-09-05T13:00",
      "departure-date": "2024-09-13T12:00", 
      "guest-names": "John and Marlena",
      "last-name-primary": "Jones",
      "number-of-guests": "3",
      "type-of-exchange": "Reciprocal",  
    }
]
```

## Return body

The following example shows the response if the `host_id` is 1 and the guest's `id` is 2.

```js
[
    {
      "host_id": 1,
      "arrival-date": "2024-09-05T13:00",
      "departure-date": "2024-09-13T12:00", 
      "guest-names": "John and Marlena",
      "last-name-primary": "Jones",
      "number-of-guests": "3",
      "type-of-exchange": "Reciprocal",  
      "id": 2
    }
]
```

**Note** You can use a request like this to update `number-of-guests`. To do that, change the two parameters in the curly braces {} after the resource name in the request URL. In this resource, you can only change `guest-names` and `number-of-guests`.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated and returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
