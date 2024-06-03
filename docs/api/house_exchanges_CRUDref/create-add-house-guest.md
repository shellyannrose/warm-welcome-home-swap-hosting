# Add a house guest to the host's account

This creates a record of a new house guest for a specific host `user_id`.

## URL

```shell

{POST}{server_url}/house-exchanges/{user_id}
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | Refers to the host id in the users resource |
| `arrival-date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest arrives. Update not supported |
| `departure-date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest leaves. Update not supported |
| `guest-names` | String |The names of all the guests |
| `last-name-primary` | String |The last name of the point of contact guest. Update not supported |
| `number-of-guests` | Number |The total number of guests expected |
| `type-of-exchange` | String |Indicates if swap is reciprocal or for guest points. Optional and update not supported |

## Request headers

None

## Request body

```js
[
   {
      "user_id": 1,
      "arrival-date": "2024-09-05T13:00",
      "departure-date": "2024-09-13T12:00", 
      "guest-names": "Sarah and John",
      "last-name-primary": "Jones",
      "number-of-guests ": "3",
      "type-of-exchange ": "Reciprocal"" 
    
   }
]
```

## Return body

The following example shows the response for a host whose user_id value is 1. The information should be the same as what you placed in the request body. The response should include the new house exchange's service-generated id.

```js
[
     {
      "user_id": 1,
      "arrival-date": "2024-09-05T13:00",
      "departure-date": "2024-09-13T12:00", 
      "guest-names": "Sarah and John",
      "last-name-primary": "Jones",
      "number-of-guests ": "3",
      "type-of-exchange ": "Reciprocal",  
      "id": 2
     },
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | User data created successfully |
| 500 | Internal server error | Invalid JSON |
| 404 | Error | The requested resource does not exist |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
