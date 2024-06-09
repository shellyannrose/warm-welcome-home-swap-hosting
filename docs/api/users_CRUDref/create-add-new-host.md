# Add a new host to the service

Add a new host who subscribes to the service.

## HTTP Method

POST

## URL

```shell

{server_url}/hosts/
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | String | Host’s last name |
| `first_name` | String | Host’s first name|
| `email` | String |Host’s email address |

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body

```js

   {
    "last_name": "Anderson",
    "first_name": "Neo",
    "email": "n.matrix@example.com"
    
   }

```

## Return body

The following example shows the response. The information should be the same as what you placed in the request body. The response should include a new host's service-generated id for the host.

```js
[
    {
        "last_name": "Anderson",
        "first_name": "Neo",
        "email": "n.matrixh@example.com",
        "id": 4
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
