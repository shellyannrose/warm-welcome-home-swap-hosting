# Remove a specific house guest from the host's account

Use the host's `host_id` and the guest `id` and remove a guest from the host's account.

## URL

```shell

{DELETE}{server_url}/guests/{host_id}/{id}

```

**Important** Use caution when you create a DELETE request.  If you do not provide an `id` parameter, you will remove all guests from a host's account. Also, you cannot delete any property for a guest. You can only delete the guest from a host's account.

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the user id in the hosts resource |
| `id` | Number | Service-generated unique ID for the guests resource|

## Request headers

None

## Request body

None

## Return body

The following example shows the response if the `host_id` is 3 and the guest's id is 4. That guest is no longer in the host's account.

```js
[
    {
      "host_id": 3,
      "arrival-date": "2024-09-04T15:00",
      "departure-date": "2024-09-08T12:00", 
      "guest-names": "Peter and Anna",
      "last-name-primary": "Stapleton",
      "number-of-guests ": "6",
      "type-of-exchange ": "Reciprocal",  
      "id": 4
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Action completed successfully |
| 202 | Accepted| Action has been queued |
| 204 | No Content| Action has been performed, but the response does not include an entity |
| 404 | Error | Specified house guest record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
