# Add a host to the service

This creates a record of a new host who subscribes to the service.

## URL

```shell

{POST}{server_url}/users/
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | String | Host’s last name |
| `first_name` | String | Host’s first name|
| `email` | String |Host’s email address |

## Request headers

None

## Request body

```js
[
   {
    "last_name": "Smith",
    "first_name": "Wallace",
    "email": "w.smith@example.com"
    
   }
]
```

## Return body

The following example shows the response. The information should be the same as what you placed in the request body. The response should include the new host's service-generate id.

```js
[
    {
        "last_name": "Smith",
        "first_name": "Wallace",
        "email": "w.smith@example.com",
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
