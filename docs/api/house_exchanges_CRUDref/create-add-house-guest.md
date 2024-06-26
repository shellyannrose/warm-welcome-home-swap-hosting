# Add a house guest to the host's account

Add a new house guest for a specific `host_id`.

## HTTP Method

POST

## URL

```shell

{server_url}/guests/

```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the host id in the hosts resource |
| `arrival-date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest arrives. Update not supported |
| `departure-date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest leaves. Update not supported |
| `guest-names` | String |The names of all the guests |
| `last-name-primary` | String |The last name of the point of contact guest. Update not supported |
| `number-of-guests` | Number |The total number of guests expected |
| `type-of-exchange` | String |Indicates if swap is reciprocal or for guest points. Optional and update not supported |

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body

```js

   {
      "host_id": 4,
      "arrival-date": "2050-09-05T13:00",
      "departure-date": "2090-09-13T12:00", 
      "guest-names": "Sarah Conner",
      "last-name-primary": "Reese",
      "number-of-guests ": 3,
      "type-of-exchange ": "Guest Points"
    
   }

```

## Return body

The following example shows the response for a host whose `host_id` is 1. The information should be the same as what you placed in the request body. The response should include a new service-generated id for the guest.

```js
[
     {
      "host_id": 4,
      "arrival-date": "2050-09-05T13:00",
      "departure-date": "2090-09-13T12:00", 
      "guest-names": "Sarah Conner",
      "last-name-primary": "Reese",
      "number-of-guests ": 3,
      "type-of-exchange ": "Guest Points",  
      "id": 1
     }

]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | User data created successfully |
| 500 | Internal server error | Invalid JSON |
| 404 | Error | The requested resource does not exist |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
