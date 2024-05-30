---
layout: page
---
# Add a host to the service

This creates a record of a new host who subscribes to the service.

## URL

```shell

{server_url}/users/
```

## Params

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | String | Host’s last name |
| `first_name` | String | Host’s first name|
| `email` | String |Host’s email address |

## Request headers

None

## Request body example

```js
[
   {
    "last_name": "Smith",
    "first_name": "Wallace",
    "email": "w.smith@example.com",
    
   }
]
```

## Return body example

The following example shows the response. Note that the information should be the same as you used in your request body. The response should include the new user’s service-generate id. The user’s id is automatically generated when the user is created.

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

Related information

* Add details for a new house exchange guest
* Add a task to prepare for a guest
