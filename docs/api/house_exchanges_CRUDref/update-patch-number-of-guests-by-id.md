# Update (PATCH) the total number of people coming with a guest

Use the host's `host_id` and the guest `id` and change the number of guests.

## URL

```shell

{PATCH}{server_url}/guests?host_id={value}&id={value}

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

**Important** This request only changes the properties that you place in the request body. All other properties stay the same.

```js
[
    {
      "number-of-guests": 5      
    }
]
```

## Return body

The following example shows the response if the `host_id` is 2 and the guest `id` is 3.

```js
[
    {
      "host_id": 2,
      "arrival-date": "2024-08-07T11:00",
      "departure-date": "2024-08-14T12:00", 
      "guest-names": "Pat",
      "last-name-primary": "Brent",
      "number-of-guests": "5",
      "type-of-exchange": "Guest Points",  
      "id": 3
    }
]
```

**Note** You can use a request like this to update `guest-names`. In this resource, you can only change `guest-names` and `number-of-guests`.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated and returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
