# Find hosts using the last_name parameter

Use the `last_name` parameter to get a list of hosts that have a specific last name.

## URL

```shell

{GET}{server_url}/users/{last_name}
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | String | Host’s last name |

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

**Note** You can use a similar request to find a host by  `first_name,` `email,` and `id`. Just replace the parameter in the curly braces {} at the end of the URL in the GET request.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
