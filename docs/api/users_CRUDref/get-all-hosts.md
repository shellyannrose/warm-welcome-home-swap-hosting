# Get a list of all hosts in the service

Get a list of all hosts who subscribe to the service.

## HTTP Method

GET

## URL

```shell

{server_url}/hosts/

```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

The following example shows the response.

```js
[
    {
      "last_name": "Smith",
      "first_name": "Wallace",
      "email": "w.smith@example.com",
      "id": 1
    },
    {
      "last_name": "Gibson",
      "first_name": "Harley",
      "email": "h.gibson@example.com",
      "id": 2
    },
    {
      "last_name": "Brennon",
      "first_name": "Barbara",
      "email": "b.brennon@example.com",
      "id": 3
    },
    {
      "last_name": "Weimann",
      "first_name": "Nicki",
      "email": "n.weimann@example.com",
      "id": 4
    }
]
  ```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | The requested resource does not exist |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
