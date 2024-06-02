# Update (PATCH) a specific host's email

Use the host's service-generated `id` parameter and change the email address for that host.

## URL

```shell

{PATCH}{server_url}/users/{id}
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | Number | Service-generated unique ID for the host |

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body

**Important** This request only changes the properties that you place in the request body. All other properties stay the same.

```js
[
    {
      "email": "nicki.weimann@example.com"      
    }
]
```

## Return body

The following example shows the response if the `id` parameter value is 4.

```js
[
    {
      "last_name": "Weimann",
      "first_name": "Nicholas",
      "email": "nicki.weimann@example.com",
      "id": 4
    }
]
```

**Note** You can use a similar request to update a host's `first_name` and `last_name`.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated and returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
