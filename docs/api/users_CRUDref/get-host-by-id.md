# Find a specific host using the id parameter

Use the host's `id` parameter to get information about a specific host.

## URL

```shell

{GET}{server_url}/hosts/{id}
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | Number | Service-generated unique ID for the host |

## Request headers

None

## Request body

None

## Return body

The following example shows the response if the `id` parameter value is 4.

```js
[
    {
      "last_name": "Weimann",
      "first_name": "Nicki",
      "email": "n.weimann@example.com",
      "id": 4
    }
]
```

**Note** You can use a request like this to find a host by `first_name,` `email,` and `last_name`. Just replace the parameter in the curly braces {} in the request URL.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
