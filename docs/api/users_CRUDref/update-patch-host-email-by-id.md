# Update (PATCH) a specific host's email

Change only the email address for a specific host's `id`.

## HTTP Method

PATCH

## URL

```shell

{server_url}/hosts/{id}
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
    {
      "email": "nicki.weimann@example.com"      
    }
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

**Note** You can use a request like this to update a host's `first_name` and `last_name`. Just replace the parameter in the curly braces {} in the request URL.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated and returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
