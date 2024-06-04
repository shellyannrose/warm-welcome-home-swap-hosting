# Remove a specific host from the service

Use the host's `id` parameter and remove the host from the service.

## URL

```shell

{DELETE}{server_url}/hosts/{id}

```

**Important** Use caution when you create a DELETE request.  If you do not provide an `id` parameter, you will remove all hosts from the service. Also, you cannot delete any property for a host. You can only delete the host from the service.

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | Number | Service-generated unique ID for the host |

## Request headers

None

## Request body

None

## Return body

The following example shows the response if the `id` parameter value is 2. That host is no longer subscribed to the service.

```js
[
    {
      "last_name": "Gibson",
      "first_name": "Harley",
      "email": "h.gibson@example.com",
      "id": 2
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Action completed successfully |
| 202 | Accepted| Action has been queued |
| 204 | No Content| Action has been performed, but the response does not include an entity |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
