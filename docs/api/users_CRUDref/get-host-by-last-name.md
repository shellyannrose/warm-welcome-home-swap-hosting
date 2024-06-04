# Find hosts using the last_name parameter

Use the `last_name` parameter to get a list of hosts that have a specific last name.

## URL

```shell

{GET}{server_url}/hosts?{parameter}={value}
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | String | Host's last name |

## Request headers

None

## Request body

None

## Return body

The following example shows the response for all hosts whose `last_name` parameter value is Brennon.

```js
[
    {
      "last_name": "Brennon",
      "first_name": "Barbara",
      "email": "b.brennon@example.com",
      "id": 3
    }
]
```

**Note** You can use a request like this to find a host by a specific `first_name,` `email,` and `id`. After the question mark, change the parameter name and value in the request URL.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
