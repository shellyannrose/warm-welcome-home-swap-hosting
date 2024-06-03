# Remove a specific house guest from the host's account

Use the host's `user_id` and the house guest's `id` and remove the guest from the host's account.

## URL

```shell

{DELETE}{server_url}/house-exchanges/{user_id}/{id}

```

**Important** Use caution when you create a DELETE request.  If you do not provide an `id` parameter, you will remove all house guests from a host's account. Also, you cannot delete any property for a house guest. You can only delete the house guest from a host's account.

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | Refers to the host id in the users resource |
| `id` | Number | Service-generated unique ID for the house guest |

## Request headers

None

## Request body

None

## Return body

The following example shows the response if the `user_id` value is 3 and the `id` value is 4. That house guest is no longer in the host's account.

```js
[
    {
      "user_id": 3,
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
