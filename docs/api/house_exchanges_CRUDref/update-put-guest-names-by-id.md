# Update (PUT) guest names

Use the host's `user_id` and the house-exchanges `id` and change the guest names.

## URL

```shell

{PUT}{server_url}/house-exchanges/{user_id}/{id}
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | Refers to the host id in the users resource |
| `id` | Number | Service-generated unique ID for the host |

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

The following example shows the response if the host's `user_id` is 1 and the house-exchanges `id` is 2.

```js
[
    {
      "user_id": 1,
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

**Note** You can use a similar request to update `number-of-guests`. In this resource, you can only change `guest-names` and `number-of-guests`.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated and returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
