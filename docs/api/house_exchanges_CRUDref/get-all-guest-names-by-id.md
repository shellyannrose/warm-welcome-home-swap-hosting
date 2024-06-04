# Find all guest names for a specific guest

Use the host's `host_id`, the guest's `id`, and `guest-names` to get a list of all the guests' names.


## URL

```shell

{GET}{server_url}/guests/{host_id}/{id}/guest-names

```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the host id in the hosts resource |
| `id` | Number | Service-generated unique ID for the guests resource |

## Request headers

None

## Request body

None

## Return body

The following example shows the guest names for the host whose `host_id` is 3 and guest id is 4.

```js
[
     {
      "user_id": 3,
      "guest-names": "Peter and Anna",      
      "id": 4
    }
]
```


**Note** You can use a request like this to find a specific guest's details. These include `arrival-date`,`departure-date`,`last-name-primary`, `number-of-guests`, and `type-of-exchange`. To do that, change the two parameters in the curly braces {} after the resource name in the request URL. Then change the final parameter after the forward slash in the URL.


## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
