# Find all guest names for a specific guest

Use the host's `user_id`, the house-exchanges `id`, and `guest-names` to get a list of all the guests' names.

## URL

```shell

{GET}{server_url}/house-exchanges/{user_id}/{id}/guest-names
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | Refers to the host id in the users resource |
| `id` | Number | Service-generated unique ID for the house exchange |

## Request headers

None

## Request body

None

## Return body

The following example shows the guest names for the host whose `user_id` is 3 and `house-exchanges` id is 4.

```js
[
     {
      "user_id": 3,
      "guest-names": "Peter and Anna",      
      "id": 4
    }
]
```

**Note** You can use a similar request to find a specific guest's details. These include `arrival-date`,`departure-date`,`last-name-primary`, `number-of-guests`, and `type-of-exchange`. Just replace the last two parameters in the curly braces {} in the URL in the GET request.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
